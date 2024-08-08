---
title: "ProgParm class                | QSYS API Reference Guide"
description: "Represents a parameter in a program call in a DataLink connection. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents a parameter in a program call in a DataLink connection.

**Namespace:** ASNA.DataGate.DataLink
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [ProgParm](#progparmprogparmtype-datadirection)([ProgParmType](/reference/datagate/datagate-data-link/prog-parm-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html)) | Initializes a new instance of the  class with the specified parameter type and data direction.
| [ProgParm](#progparmstructuretype-datadirection)([StructureType](/reference/datagate/datagate-data-link/structure-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html)) | Initializes a new instance of the  class with the specified structure type and data direction.

### ProgParm([ProgParmType](/reference/datagate/datagate-data-link/prog-parm-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html))

Initializes a new instance of the  class with the specified parameter type and data direction.

```cs
ProgParm(ProgParmType, DataDirection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParmType](/reference/datagate/datagate-data-link/prog-parm-type.html) | ppt | The type of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | dir | The direction of the data (input, output, or both).

### ProgParm([StructureType](/reference/datagate/datagate-data-link/structure-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html))

Initializes a new instance of the  class with the specified structure type and data direction.

```cs
ProgParm(StructureType, DataDirection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [StructureType](/reference/datagate/datagate-data-link/structure-type.html) | st | The structure type of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | dir | The direction of the data (input, output, or both).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | Direction | Gets or sets the direction of the data for this parameter (input, output, or both). |

## Example 1.Passing three parameters to an AS400 Program


```cs 
  /* Create paramerter list to send to the program being called.
   * The first two parameters catch return values, the last will tell the
   * external program to shut down if the value is '1'. */
  char Quit400App = '1';

  ProgParm[] parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input)
  };

  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");
  prog.AppendParms(parms); //Use our parm list defined above.
  //Here, we make sure our variables are passed as the parms in ther parm list.
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  //Now we execute the call to the As400Program, "Call400".
  prog.Execute();
```

