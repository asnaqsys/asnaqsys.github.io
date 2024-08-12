---
title: "QSYS Database File Essentials"
description: "Explore the core aspects of QSYS database files in IBM i systems. This guide covers creation, management, and best practices for efficient database handling and optimization."
---

IBM i RPG [File Description Specifications](https://www.ibm.com/docs/en/i/7.2?topic=specifications-file-description) are implemented in `ASNA.QSys` by the class `DatabaseFile`.

> Note: **Program Described** files are converted to **Externally Described** files during Migration.

`ASNA.QSys.DatabaseFile` provides the expected methods to perform classical RPG I/O operations, including:
* Open/Close
* Chain (Read by Key)
* Write
* Read / ReadNext / ReadPrevious / Read Equal, etc.
* Update
* Delete

> You can get detailed information on any method reading [QSys Reference]()

Topics that deserve further explanation in the use of DatabaseFile classes are:
1. How are DatabaseFile classes *Instanced* ?
2. When are *Implicit Open* files Open and Closed ?
3. How are *class field*s for DatabaseFile *automatically* declared ?
4. How are *Physical* and *Logical* files located in the connected ASNA.DataGate.Client *DBName* ?
5. How are files *Bound* to *Data Structures* ?
6. How does *File Override* work ?

## DatabaseFile Object Allocation
Every migrated Program takes the form of a subclass derived from `ASNA.QSys Program` (or `ASNA.QSys CLProgram`), with a *constructor* method similar to this:

```cs
public myLegacyProgramName()
{
    _IN = new IndicatorArray<Len<_1, _0, _0>>((char[])null);
    _instanceInit();

    .
    .
    .
}
```

Where the implementation of `_instanceInit()` is explicitly generated at the bottom of the class, with contents similar to the following code:

```cs
void _instanceInit()
{
    .
    .
    .
    MYLEGACYFILE1 = new DatabaseFile(PopulateBufferMYLEGACYFILE1, PopulateFieldsMYLEGACYFILE1, null, "MYLEGACYFILE1", "*LIBL/MYLEGACYFILE1", MYLEGACYFILE1FormatIDs)
    { IsDefaultRFN = true };

    MYLEGACYFILE2 = new DatabaseFile(PopulateBufferMYLEGACYFILE2, PopulateFieldsMYLEGACYFILE2, null, "MYLEGACYFILE2", "*LIBL/MYLEGACYFILE2", MYLEGACYFILE2FormatIDs, blockingFactor : 0)
    { IsDefaultRFN = true };
}
```
Where,

* MYLEGACYFILE1 and MYLEGACYFILE2 are class fields declared of type `DatabaseFile` (uninitialized).

* `PopulateBufferXXX` and `PopulateFieldsXXX` where *XXX* is the name of the field (MYLEGACYFILE1 in this case), are methods generated in a [partial class](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods) with the purpose of updating the record fields declared in the `myLegacyProgramName` to be used as individual fields in the calculation logic of this program (explained in detail in the next section on this page).

* `XXXFormatIDs` where *XXX* is the name of the field (MYLEGACYFILE1 in this case), are [Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-5.0) instances with statically computed *Record Format Level Identifier*[^1] for the records defined by file *XXX*.

* `"*LIBL/XXX"` where *XXX* is the name of the field (MYLEGACYFILE1 in this case),
is the search *path* to locate the external *object*. `"XXX"` in this case represents the Operating System *object* name (Physical or Logical *File* - *Table* or *View* - on the Database). `"*LIBL"` means, use the [Library List](https://www.ibm.com/docs/en/i/7.2?topic=security-library-lists). For detailed explanation read [ASNA.QSys.DataGate.Client Reference]().

>For details on other parameters, read [ASNA.QSys.Runtime Reference]() 

## Opening and Closing file implementation
As expected on any C# class, the *constructor* and the *dispose* methods are used to *initialize* and *clean-up* resources, in this case `Open` and `Close` files.

> Only files declared as *Implicit Open* are included in the *constructor*. 

The *constructor* and the *dispose* templated code looks like the following code:

```cs
#region Constructor and Dispose 
    public myLegacyProgramName()
    {
            .
            .
            .

        MYLEGACYFILE1.Overrider = Job;
        MYLEGACYFILE1.Open(Job.Database, AccessMode.RWCD, false, false, ServerCursors.Default);

        MYLEGACYFILE2.Overrider = Job;
        MYLEGACYFILE1.Open(Job.Database, AccessMode.Read, false, false, ServerCursors.Default);

            .
            .
            .
    }

    override public void Dispose(bool disposing)
    {
        if (disposing)
        {
            .
            .
            .
            MYLEGACYFILE1.Close();
            MYLEGACYFILE2.Close();
        }
        base.Dispose(disposing);
    }
#endregion
```

For *Disposal*, it is assumed that `DatabaseFile` fields have been *instanced* inside the method `_instanceInit()`.

> It is harmless to `Close` a `DatabaseFile` field if the file is not Open.

The `Overrider` property is explained later.

## Database fields automatic declaration

IBM i RPG compiler generated code that was not visible to the IBM i Developer, to assist with the [Application Development model](/concepts/background/ibmi-developer-model.html). In particular:

> &#128161; For every **field** on every **record** defined by any externally described **file**, a stand alone field was declared which was *bound* to the *active* record at execution time.

The C# Language does not provide the same integrated database file support as IBM i RPG, by definition C# is a [General Purpose Programming Language](https://en.wikipedia.org/wiki/General-purpose_programming_language).

Initially - *during migration* - the generated class derived from `ASNA.QSys Program` is completed with the database file support - available in RPG - by means of C# [partial class](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods).

As the Application is maintained - if [database schema](https://en.wikipedia.org/wiki/Database_schema) changes -, the **partial** generated classes need to be **re-generated**. The later is done by manually running *Monarch Dev Tools* (explained later in this page).

**EXTRACTION OF FILE SCHEMA**

Every RPG Program migrated, produces **three** files:

1. MY_PROGRAM.cs - class declaration with constructor, dispose and migrated RPG *Business Logic*.
2. MY_PROGRAM.Io.xfu - stand-alone XML file with detailed external *file usage* information.
3. MY_PROGRAM.Io.cs - partial class completing the declaration of fields for external files and implementation of I/O PopulateBufferXXX and PopulateFieldsXXX methods for all records to implement [data binding](https://en.wikipedia.org/wiki/Data_binding), the RPG *way*.

The *MY_PROGRAM.cs* is the class body that we have been discussing in previous sections.

**XFU STATIC RECORD USAGE**

During Migration, the set of 'externally described' files used by a program and the usage of each file are written into an XML file that is later used to generate the *MY_PROGRAM.Io.cs* partial class.  

>In addition to *Database Schema* XFU files contain information about how externally described Data-Structures are mapped into records of the database, according to RPG [Definition Specifications](https://www.ibm.com/docs/en/i/7.2?topic=specifications-definition)

To generate the *MY_PROGRAM.Io.cs* partial class the ASNA Tools use *MY_PROGRAM.Io.xfu* to declare using C# syntax, field declaration of the types defined by the [Fixed Types](/concepts/program-structure/qsys-fixedtypes.html).

> It is assumed that field names - across records - do not collide, RPG had ways to rename fields to avoid collisions.

The partial class looks similar to the following code:

```cs
namespace MyCompany.MyApplication
{
    
    public partial class myLegacyProgramName
    {
        private FixedDecimal<_9, _0> CMCUSTNO;
        private FixedString<_40> CMNAME;
        private FixedString<_35> CMADDR1;
        private FixedString<_35> CMADDR2;
        private FixedString<_30> CMCITY;
        private FixedString<_2> CMSTATE;
        private FixedString<_10> CMPOSTCODE;
        private FixedString<_1> CMACTIVE;
        private FixedDecimal<_10, _0> CMFAX;
        private FixedString<_20> CMPHONE;
        private FixedString<_5> CMUSRFLGS;
        private FixedString<_40> CMCONTACT;
        private FixedString<_40> CMCONEMAL;
        private FixedString<_1> CMYN01;
        private FixedString<_1> CMYN02;
        private FixedString<_1> CMYN03;
```

The `Fixed`XXX where *XXX* is the .NET-*like* data type is described [Here](/concepts/program-structure/qsys-fixedtypes.html).

The names of the *fields* are **ALL** fields in **records** defined according to the **file** schema. The types, lengths, precision etc. are *static snapshots* of the state of the Database *schema* when the Program was Migrated (more specifically converted to C#).

**THE I/O BUFFER**

As discussed in the concept [Workstation file](/concepts/program-structure/qsys-workstationfile.html), the only *shared* abstraction of the Data between the Presentation Layers and the Business Logic is the [DataSet](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/dataset-datatable-dataview/).

The **DatSet** is a collection of all **DataTable**s as defined by the records in each file.

The **DataTable** is a collection of **DataRow**s which are records that have been read from the file. 

Referring to the concept [RPG language-provided Display and Database support](/concepts/program-structure/rpg-language-files.html), where we touched on the topic `one-record-at-a-time` access, RPG normally deals with one record per Table, known as the *Active* record, or *I/O Buffer*[^2].

The *I/O* Buffer for a file, is the *Active* **DataRow** of the *DataTable*.

**POPULATE METHODS TRIGGERED BY I/O OPERATIONS**

There are two operations that need to be executed when data flows between the I/O Buffers and their corresponding Program fields:

1. Update the fields using the current values in the I/O Buffer - file has just been read.
2. Update the I/O Buffer with the possibly changed field values - file has just been written to.

> I/O Operations call behind the scenes the proper *Populate* methods. You do not *normally* need to worry about the internal mechanics. The Developer's only concern should be to keep the XFU and partial class generated code updated, when the file schema changes.

The following methods show the two *Populate* methods invoked indirectly when performing I/O operations on file **MYLEGACYFILE1** (a sample instance of DatabaseFile class):

```cs
private void PopulateFieldsMYLEGACYFILE1(string _, AdgDataSet _dataSet)
{
    var _table = _dataSet.SetActive("*FILE");
    System.Data.DataRow _row = _table.Row;
    CMCUSTNO = ((decimal)(_row["CMCUSTNO"]));
    CMNAME = ((string)(_row["CMNAME"]));
    CMADDR1 = ((string)(_row["CMADDR1"]));
    CMADDR2 = ((string)(_row["CMADDR2"]));
    CMCITY = ((string)(_row["CMCITY"]));
    CMSTATE = ((string)(_row["CMSTATE"]));
    CMPOSTCODE = ((string)(_row["CMPOSTCODE"]));
    CMACTIVE = ((string)(_row["CMACTIVE"]));
    CMFAX = ((decimal)(_row["CMFAX"]));
    CMPHONE = ((string)(_row["CMPHONE"]));
    CMUSRFLGS = ((string)(_row["CMUSRFLGS"]));
    CMCONTACT = ((string)(_row["CMCONTACT"]));
    CMCONEMAL = ((string)(_row["CMCONEMAL"]));
    CMYN01 = ((string)(_row["CMYN01"]));
    CMYN02 = ((string)(_row["CMYN02"]));
    CMYN03 = ((string)(_row["CMYN03"]));
}
```

```cs
private void PopulateBufferMYLEGACYFILE1(string _, AdgDataSet _dataSet)
{
    var _table = _dataSet.GetAdgTable("*FILE");
    System.Data.DataRow _row = _table.Row;
    _row["CMCUSTNO"] = ((decimal)(CMCUSTNO));
    _row["CMNAME"] = ((string)(CMNAME));
    _row["CMADDR1"] = ((string)(CMADDR1));
    _row["CMADDR2"] = ((string)(CMADDR2));
    _row["CMCITY"] = ((string)(CMCITY));
    _row["CMSTATE"] = ((string)(CMSTATE));
    _row["CMPOSTCODE"] = ((string)(CMPOSTCODE));
    _row["CMACTIVE"] = ((string)(CMACTIVE));
    _row["CMFAX"] = ((decimal)(CMFAX));
    _row["CMPHONE"] = ((string)(CMPHONE));
    _row["CMUSRFLGS"] = ((string)(CMUSRFLGS));
    _row["CMCONTACT"] = ((string)(CMCONTACT));
    _row["CMCONEMAL"] = ((string)(CMCONEMAL));
    _row["CMYN01"] = ((string)(CMYN01));
    _row["CMYN02"] = ((string)(CMYN02));
    _row["CMYN03"] = ((string)(CMYN03));
}
```
## File Overriding

IBM i [File Overriding](https://www.ibm.com/docs/en/i/7.2?topic=overrides-summary-override-commands) is a technique that directs the Operating System to locate different *Objects* that those used to compile a Program. This is *similar* to the concept [URL Redirection](https://en.wikipedia.org/wiki/URL_redirection) more commonly known to Web Developers.

>Program behavior can be affected without recompiling, by requesting the Operating System to change how external resources are located and used.

File Overriding on IBM i is done with commands executed at the prompt *or* as part of Programs written in CL.

The RPG Business Logic, needs to *Apply* the override rules, before opening files.

If you look again at any *constructor* code on **ANY** of the Migrated Programs (derived from class `ASNA.QSys Program`), you will see code like the following:

```cs
public myLegacyProgramName()
{
    _IN = new IndicatorArray<Len<_1, _0, _0>>((char[])null);
    _instanceInit();

        .
        .
        .

    MYLEGACYFILE1.Overrider = Job;
    MYLEGACYFILE1.Open(Job.Database, AccessMode.RWCD, false, false, ServerCursors.Default);
    
    MYLEGACYFILE2.Overrider = Job;
    MYLEGACYFILE2.Open(Job.Database, AccessMode.Read, false, false, ServerCursors.Default);
}

```

The line `MYLEGACYFILE1.Overrider = Job;` and `MYLEGACYFILE2.Overrider = Job;` is setting the property `Overrider` of the class `DatabaseFile` to the Job reference. This is done, to prepare the file instance for operations such as `Open`.

> When changing code during maintenance, make sure to leave the `Overrider` setter code before **ANY** call to any I/O methods.

## Monarch Dev Tools to assist in File maintenance

There are two external tools provided by ASNA that are available when changing **file** schema[^3]:

1. Refresh XFU
2. Run Custom Tool (for a Program source file).

* Refresh XFU - For **every** file field in the Program (database, workstation and printfiles), *get* the current schema(s) from the external physical devices and write the XML file.

* Custom Tool - The tool that is configured to run for `.cs` source files that have classes derived from `ASNA.QSys Program`, is a tool that takes the XML definition of the schema and data structure mapping information - *XFU* file - and **re-generates** the `partial` class in the `.Io.cs` related source file. (Recall that the partial class defines Program fields according to file schema records and *PopulateXXX* I/O methods).

> If possible, avoid changing *manually* the contents of the `.Io.cs` partial classes, letting the Custom Tool freely replace the proper source.

<br>
<br>
<br>

[^1]: *Record Format Level Identifier* is a IBM i proprietary record hash calculation, that uniquely identifies the fields, lengths and types. Used by the Operating System as a mechanism to check the *version* of the external references of a Program, such that, if the compilation happened with an *incompatible* version, the execution is stopped, to prevent invalid runs.
[^2]: Subfile records are the exception. These may contain several records at one time.
[^3]: In the case of WorkstationFile changing fields in the `PageModel` class is also considered a schema change.  