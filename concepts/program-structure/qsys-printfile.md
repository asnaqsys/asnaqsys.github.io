---
title: "Guide to QSYS Print Files Management"
description: "Master QSYS print files with our comprehensive guide. Learn to create, configure, and manage print files for optimal output."
---

`ASNA.QSys.Printfile` or `QSys Printfile` (for short), is the ASNA.QSys class that abstracts the concept of a [IBM i Printer file](https://www.ibm.com/docs/en/i/7.3?topic=file-printer-overview).

Similarly to a [QSys DatabaseFile](/concepts/program-structure/qsys-databasefile.html), a `QSys Printfile` is a class used to instance objects to produce output records, according to external definitions.

## External Definition of a DataGate .NET Printer file
The QSys Printfile obtains its general characteristics like field definitions, page layout, printer attributes from a DataGate .NET Printerfile.

A DataGate .NET Printer File is composed of one or more record formats, each defining a template of what is to be shown in a segment of the page.  A record format is a collection of fields.  Each field is within a record is embodied by a .NET control.   The definition of a Printer file is kept as part of a DataGate database.

### Creating/Designing `DataGate Printfile` objects
Microsoft Visual Studio (with DataGate integration) is used to create and maintain .NET Printfiles.

## Using PrintFiles in a QSys Program.
To access Printfiles in a `QSys Program`, objects of the [QSys.Printfile] class are used. 
Programs typically declare the object as a member of the Program with code like:

**Declaration**
```cs
namespace MyCompany.MyApplication
{
    [ASNA.QSys.HostServices.ActivationGroup("*DFTACTGRP")]
    [ProgramEntry("_ENTRY")]
    public partial class MyProgram : ASNA.QSys.HostServices.Program
    {
        PrintFile QPRINT;
```

**Printfile Object Instantiation**

The declaration of the printfile as indicated above, has the PrintFile object set to null. As we have described in the topic [QSys DatabaseFile](/concepts/program-structure/qsys-databasefile.html), the .NET Printfile object is *Instanced* in the [RPG language support](/concepts/program-structure/rpg-language-files.html) generated method `_instanceInit`, as follows: 

```cs
void _instanceInit()
{
    .
    .
    .
    QPRINT = new PrintFile(PopulateBufferQPRINT, "QPRINT", "MYLIBRARY\\MYFILEOBJ", QPRINTFormatIDs);
}
```
The `PrintFile` class constructor has the following required parameters:

| **Parameter**            | **Description**
| ------------------------ | ---
| populateBufferMethod     | method called internally by I/O operations when writing.
| dclPrintFileName         | *string* logical name (usually short name).
| filePath                 | *string* library and name path to database location.
| levelCheck               | *dictionary* Level Check hash codes.

The first parameter is the name of the method generated by [Dev Tools](/concepts/enhancements/dev-tools.html). As explained in the Topic [QSys DatabaseFile](/concepts/program-structure/qsys-databasefile.html), each time code in the `Program` writes to a record, the `PopulateBuffer` partial class generated *I/O* method wil be called, to prepare the internal buffer such that the *DataSet* can be loaded to effect the external Printfile.

The second parameter `dclPrintFileName` is a short name logically representing the external printfile name. This string identifier may be used later to form paths (for output file spooling).

The third parameter `filePath` is s string *library* and *name* path to where the printfile is defined externally in the database. 

The last required parameter is a [.NET Dictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-5.0) with the [hash](https://en.wikipedia.org/wiki/Hash_function) codes have been loaded to be used while [Detecting File Description changes](https://www.ibm.com/docs/en/i/7.3?topic=files-detection-file-description-changes). This codes are also *generated* by [Dev Tools](/concepts/enhancements/dev-tools.html).

>Note the *naming convention* use by the tools, the Printfile member is used while naming the partial I/O names. In this example, `QPRINT` is used in the names: PopulateBufferQPRINT and QPRINTFormatIDs

 **Program Constructor Code**

Before a .NET Printfile can be opened for writing, there are a few required properties that need to be setup.

Let's look at the typical code that goes into every `QSys Program`'s constructor (related to printfiles):

```cs
public MyProgram()
{
    .
    .
    .
    QPRINT.Printer = "Microsoft Print to PDF";
    QPRINT.Overrider = Job;
    QPRINT.ManuscriptPath = ASNA.QSys.HostServices.Program.Spooler.GetNewFilePath(QPRINT.DclPrintFileName);
    QPRINT.Open(Job.PrinterDB);
}
```

The `Printer` property should have the name of the [Printer Driver](https://en.wikipedia.org/wiki/Printer_driver) existing in the server where the Application will be deployed.

> During development be aware that when the Application is deployed the available Print Drivers may be different in the deployment server.

The `Overrider` property should have the instance of the running [QSys Job](/concepts/architecture/qsys-job.html).

> Pay attention to the method `getPrinterDB` in `MyJob.cs`. It should return the instance of the DataGate Database Name where the .NET Printfile definitions exist. [See QSys Architecture](/concepts/architecture/qsys-job.html)

The `ManuscriptPath` is a string with the Operating System's path to the folder structure used for Program Spooling.

Finally, the .NET Printfile is **opened** in the Program's constructor. The Printfile object instantiation should have been done properly and the Printfile object's required properties should have the right values. Opening means to find the external description and prepare the Printfile to be written to.

**Destructor**

The Program *Destructor* is implemented in the method **Dispose** that gets called during [.NET Garbage Collection](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)). When a Program is *Deactivated*, it is marked as *disposable* to the .NET garbage collector. When memory needs to be reclaimed, the `Dispose` method will be called.

```cs
override public void Dispose(bool disposing)
{
    if (disposing)
    {
        .
        .
        .        
        QPRINT.Close();
    }
    base.Dispose(disposing);
}
```

Closing a Printfile does not take any parameters. It it als safe to `Close` a Printfile that was already closed (or never opened). When using a [PDF](https://en.wikipedia.org/wiki/PDF) Print Driver, the `Closing` of the Printfile will trigger I/O events, such as flushing contents, and completing creating the **PDF** file. (There may be other events triggered associated with File Spooling).


**Writing records**

Writing is no different that any other file (like [WorkstationFile](/reference/qsys-worstationfile.html) or [DatabaseFile](/reference/qsys-printfile.html) ), the Program implements logic that:
1. Sets values to the fields defined in the .NET Printfile records.
2. The method `Write` is called.

For example, the code:

```cs
wCUSTNO = EditCode.Apply(pCUSTNO, 0, 9, EditCodes.Z, "").Trim() + " " + CMNAME;
wORDNBR = EditCode.Apply(pORDNBR, 0, 9, EditCodes.Z, "").Trim();
QPRINT.Write("PrtNmeLine", _IN.Array);
```

Sets the .NET Printfile fields `wCUSTNO` and `wORDNBR` defined in record format `PrtNmeLine`. Notice how fields in .NET Printfiles are also [Fixed Types](/concepts/program-structure/qsys-fixedtypes.html) as defined by Legacy DDS which may need formatting according to [Edit codes in printer files](https://www.ibm.com/docs/en/i/7.1?topic=files-i-edit-codes-in-printer).

> QSys Fixed Types do automatic conversion from/to C# *string* types.

Writing to the .NET Printfile requires the [Indicators](/concepts/program-structure/qsys-program.html). This is needed to evaluate conditional writing of fields in the printfile.

**Checking for Page Overflow**

.NET Printfile design defines the *Overflow* page area. This is the area from the bottom of the Page where no printing should happen. 

Generated QSys derived Application Programs define a member field called:

```cs
Indicator _INOF;
```

This is the Page *Overflow Indicator*. The Application Program needs to update the state of this *Indicator* after every `Write` operation to any of the Printfiles.

Code generation is very consistent, after a `Write` method call, there will always be the following property setter:

```cs
QPRINT.Write("MyRecordName", _IN.Array);
_INOF = (Indicator)QPRINT.InOverflow;
```

To update `_INOF`, the current value of the Printfile indicator is read. The property `InOverflow` of the PrintFile object returns if the *next* print line will fall into the non-printable area of the page.

> When adding code manually, don't forget to update the `_INOF` indicator.


