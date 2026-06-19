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


