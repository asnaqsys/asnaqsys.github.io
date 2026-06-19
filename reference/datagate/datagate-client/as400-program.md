---
title: "As400Program class"
description: "Represents a program in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents a program in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

## Remarks
This class provides methods and properties to manage a program in the ASNA DataGate client. 
It includes methods to set the program path and connection, execute the program, 
get and append parameters, convert parameters to and from objects, set parameters to zero value, 
and read and write parameters in XML format. It also implements the IDisposable interface, 
which provides a mechanism for releasing unmanaged resources.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [As400Program()](as400-program-ctor.html#as400program) | Initializes a new instance of the  class.
| [As400Program](as400-program-ctor.html#as400program-adgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the  class with the specified connection.
| [As400Program](as400-program-ctor.html#as400program-adgconnection-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified connection and program path.

## Methods

| Signature | Description |
| --- | --- |
| [AppendParm](as400-program-appendparm.html#void-appendparm-progparm-parameter)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends a parameter to the program.
| [AppendParm](as400-program-appendparm.html#void-appendparm-progparm-parameter-2)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends a parameter to the specified list of parameters.
| [AppendParms](as400-program-appendparms.html#void-appendparms-progparm-parameters-reference-datagate-datagate-data-link-prog-parm-html)([ProgParm\[\]](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends an array of parameters to the program.
| [Dispose()](as400-program-dispose.html#void-dispose) | Releases all resources used by the current instance of the  class.
| [Dispose](as400-program-dispose.html#void-dispose-bool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the unmanaged resources used by the  and optionally releases the managed resources.
| [Execute()](as400-program-execute.html#void-execute) | Executes the program with the current parameters.
| [Finalize()](as400-program-finalize.html#void-finalize) | Finalizes an instance of the  class.
| [GetParameters()](as400-program-getparameters.html#ienumerable-progparm-getparameters) | Gets the parameters of the program.
| [GetParmByName](as400-program-getparmbyname.html#progparm-getparmbyname-string-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the parameter with the specified name.
| [GetParmByName](as400-program-getparmbyname.html#progparm-getparmbyname-string-name-2)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the parameter with the specified name from the specified list of parameters.
| [ObjectToParm](as400-program-objecttoparm.html#void-objecttoparm-progparm-parameter-object-value-int-element)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified object to a parameter of the specified type.
| [ObjectToParm](as400-program-objecttoparm.html#void-objecttoparm-progparm-parameter-object-value)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Converts the specified object to a parameter.
| [ObjectToParm](as400-program-objecttoparm.html#void-objecttoparm-object-value-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified object to a parameter of the specified name and element indices.
| [ObjectToParm](as400-program-objecttoparm.html#void-objecttoparm-object-value-string-parametername)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified object to a parameter of the specified name.
| [ParmToObject](as400-program-parmtoobject.html#object-parmtoobject-progparm-parameter-type-returntype-int-element)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified parameter to an object of the specified type.
| [ParmToObject](as400-program-parmtoobject.html#object-parmtoobject-progparm-parameter-type-returntype)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Converts the specified parameter to an object of the specified type.
| [ParmToObject](as400-program-parmtoobject.html#object-parmtoobject-type-returntype-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified parameter to an object of the specified type.
| [ParmToObject](as400-program-parmtoobject.html#object-parmtoobject-type-returntype-string-parametername)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified parameter to an object of the specified type.
| [ReadParmXml](as400-program-readparmxml.html#void-readparmxml-xmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the parameters of the program from an XML reader.
| [SetConnection](as400-program-setconnection.html#void-setconnection-adgconnection-value)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Sets the connection to be used by the program.
| [SetParmsZeroValue()](as400-program-setparmszerovalue.html#void-setparmszerovalue) | Sets all parameters of the program to their zero value.
| [SetProgramPath](as400-program-setprogrampath.html#void-setprogrampath-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the path of the program to be executed.
| [WriteParmXml](as400-program-writeparmxml.html#void-writeparmxml-xmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the parameters of the program to an XML writer.

## Example 1. As400Program constructor method example.

```cs 
  /* Here, "ProdDB" is an initialized AdgConnection and
   * Call400 is a valid IBM i program file. */
  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");
```

## Example 2. As400Program constructor method example 2.

```cs 
  //Here, "ProdDB" is an initialized AdgConnection.
  As400Program prog = new As400Program(ProdDB);
  prog.SetProgramPath( "*Libl/Call400" );
```

## Example 3. As400Program constructor method example 3.

```cs 
  //Here, "ProdDB" is an initialized AdgConnection.
  As400Program prog = new As400Program();
  prog.SetConnection( ProdDB );
  prog.SetProgramPath("*Libl/Call400");
```

## Example 4. ParmToObject method example.

```cs 
  /* Here, Prog is an initialized As400Program object
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[3];
  Parms[0] = new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output);
  Parms[1] = new ProgParm(
        new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output);
  Parms[2] = new ProgParm(
        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input);
  prog.AppendParms(Parms);
  prog.ObjectToParm(Parms[2], Quit400App, 0);
  prog.Execute(); 
  /* After calling the last two values in the parameter list
   * will have new values in it.  To read them, we set our local
   * variables to the returned values in the parameters list. */
  CustName = Convert.ToString(
      prog.ParmToObject(System.Type.GetType("System.String"),
      "CustName",
      0));
  TimeOfDay = Convert.ToDecimal( prog.ParmToObject(System.Type.GetType("System.Decimal"),
      "TimeOfDay",
       0));
```

## Example 5. ObjectToParm method example.

```cs 
  /* Here, "prog" is an initialized As400Program object.
   * The first two lines creates a IBM i character data type whose
   * length is one, and then appends it to "prog"'s parameter list. */
  ProgParm QuitParm = new ProgParm(
        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
        DataDirection.InputOutput );
  prog.AppendParm(QuitParm);
  char QuitChar = '1';
  /* This next line assigns the .NET value, CustName, to the
   * IBM i data type of the same name in the parameter list. */
  prog.ObjectToParm(QuitParm, QuitChar, 0);

```

## Example 6. as400Program Connection property example.

```cs 
  As400Program prog = new As400Program();
  prog.SetConnection( createAdgConnection("YourIBMi") );
  prog.SetProgramPath( "*Libl/Call400" );
```


## Example  7. as400Program AppendParms method example.

```cs 
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
      DataDirection.Input)
  };
  prog.AppendParms(Parms);
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  prog.Execute();
  CustName = Convert.ToString(
     prog.ParmToObject(System.Type.GetType("System.String"),
     "CustName",
     new int[]{}));
  TimeOfDay = Convert.ToDecimal(
     prog.ParmToObject(System.Type.GetType("System.Decimal"),
     "TimeOfDay",
     new int[]{}));
             
```

## Example 8. as400Program AppendParm method example.

```cs 
  /* Here, prog is an initialized As400Program.
   * We add the field "CustName" to the parm list, and a local
   * string variable by the same name into it.  After calling the
   * program, we then set the local variable to the returned
   * value in the parms list. */
  prog.AppendParm( new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)),
        DataDirection.InputOutput
  ));
  //Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", new int[]{} );
  prog.Execute();
  //Fetch the returned value.
  CustName = Convert.ToString(
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", 
        new int[]{}));  
```


## Example 9. as400Program SetProgramPath method example.

```cs 
  As400Program prog = new As400Program();
  prog.SetConnection( createAdgConnection("YourIBMi") );
  prog.SetProgramPath = "*Libl/Call400";
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`

