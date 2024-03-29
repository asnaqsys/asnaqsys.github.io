---
title: ProgParm(ProgParmType, DataDirection)

---

Construct a representation of a simple iSeries program parameter.

```cs
 public ProgParm( ProgParmType ppt, DataDirection dir )
```


## Parameters



 *ppt* 

: 
[ProgParmType](prog-parm-type-class.html). The data type description 
						of the simple program parameter. 

 *dir* 

: 
[ASNA.DataGate.Common.DataDirection](data-direction-enumeration.html). 
								The declared input/output orientation of the parameter.


## Remarks

**ProgParm** constructors define the metadata and input/output orientation of a single iSeries program parameter. In this form, *ppt* contains the type description for the simple (non-structured) parameter.

*dir* defines the parameter as an "input" or "output" parameter, or both. This optimizes the movement of parameter value data across the client/server link as detailed by the following table:
<br />



| Value of *dir* | Data Movement |
| ---- | ---- |
| Input | Value data moves from DG to data provider prior to iSeries program call only. |
| Output | Value data moves from data provider to DG after return from iSeries program call only. |
| InputOutput | Value data moves from DG to data provider prior to iSeries program call and from data provider to DG after return from iSeries program call. |
| None | No parameter value data is transferred. |



<br />

Careful use of the *dir* parameter can improve the performance of iSeries program calls in DG. For example, by specifying **DataDirection.None** (for a parameter not used by your program nor the iSeries program), the network bandwidth required for passing that parameter across the client/server link is decreased.

**ProgParm** constructors do not allow the initialization of the parameter value data. Values may only be set in the **ProgParm** object after it has been added to the [As400Program](as400program-class.html) parameter list (via [AppendParm](as400program-class-append-parm-method.html) or [AppendParms](as400program-class-append-parms-method.html)). Use the [ObjectToParm](as400program-class-object-to_parm-method-main.html) method to set the value *data* of the **ProgParm** .
## Examples


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

## Requirements

**Namespace:** [ASNA.DataGate.DataLink](datagate-data-link-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[ProgParm Class](prog-parm-class.html)
      <br />
[ProgParm Class Members](prog-parm-members.html)
      <br />
[As400Program Class](as400program-class.html)
      <br />
[AppendParm Method](as400program-class-append-parm-method.html)
      <br />
[AppendParms Method](as400program-class-append-parms-method.html)
      <br />
[ObjectToParm Method](as400program-class-object-to_parm-method-main.html)
      <br />
[DataDirection Enumeration](data-direction-enumeration.html)
      <br />
[ASNA.DataGate.DataLink Namespace](datagate-data-link-namespace.html)
      <br />
[Calling Stored Procedures](calling-stored-procedures.html)

