---
title: "DataDirection enum            | QSYS API Reference Guide"
description: "Specifies the direction of data flow for a data operation. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the direction of data flow for a data operation.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Input | Specifies that data is flowing in. | 1 |
| InputOutput | Specifies that data is flowing both in and out. | 3 |
| None | Specifies that there is no data flow. | 0 |
| Output | Specifies that data is flowing out. | 2 |

## Examples

```cs
   AdgConnection ProdDB = createAdgConnection("YourIBMi");
   char Quit400App = '1';
   string CustName;
   decimal TimeOfDay;

  /* We know that the first two parameters will be for
   * returning values, so we set their DataDirection
   * enumeration types to Output. The third value will
   * be sent in to tell the external program whether or not
   * to quit running, but will not return a value,
   * so we set its DataDirection type to Input. */
  ProgParm[] Parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, 
          FieldType.NewChar(40)), DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, 
          FieldType.NewPacked(6, 0)), ASNA.DataGate.Common.DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, 
          FieldType.NewChar(1)), DataDirection.Input)
  };
  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");
  prog.AppendParms(Parms); //Use our parm list defined above.
  //Here, we make sure our variables are passed as the parms in ther parm list.
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  //Now we execute the call to the As400Program, "Call400".
  prog.Execute();
  //Here, we get the values from the parm list and put them back into our variables.
  CustName = Convert.ToString(prog.ParmToObject(System.Type.GetType("System.String"), 
      "CustName", new int[]{}));
  TimeOfDay = Convert.ToDecimal(prog.ParmToObject(System.Type.GetType("System.Decimal"), 
      "TimeOfDay", new int[]{}));
```

> See [AdgConnection Example](/reference/datagate/datagate-client/adg-connection.html#create-an-adgconnection) for an implementation of `createAdgConnection()`
