---
title: ProgParm(StructureType, DataDirection)

---

Construct a representation of a complex iSeries program parameter.

```cs
 public ProgParm( StructureType st, DataDirection dir )
```


## Parameters



 *st* 

: 
[StructureType](structure-type-class.html). The data type 
						description of the structured program parameter. 

 *dir* 

: 
[ASNA.DataGate.Common.DataDirection](data-direction-enumeration.html). 
								The declared input/output orientation of the parameter.


## Remarks

**ProgParm** constructors define the metadata and input/output orientation of a single iSeries program parameter. In this form, *st* contains the type description for the complex (structured) parameter.

*dir* defines the parameter as an "input" or "output" parameter, or both. This optimizes the movement of parameter value data across the client/server link as detailed by the following table:
<br />



| Value of *dir* | Data Movement |
| ---- | ---- |
| Input | Value data moves from DG to data provider prior to iSeries program call only. |
| Output | Value data moves from data provider to DG after return from iSeries program call only. |
| InputOutput | Value data moves from DG to data provider prior to iSeries program call, and from data provider to DG after return from iSeries program call. |
| None | No parameter value data is transferred. |



<br />

Careful use of the *dir* parameter can improve the performance of iSeries program calls in DG. For example, by specifying **DataDirection.None** (for a parameter not used by your program nor by your iSeries program), the network bandwidth required for passing that parameter across the client/server link is decreased.

<span> **ProgParm** </span> constructors do not allow the initialization of the parameter value data. Values may only be set in the **ProgParm** object after it has been added to the [As400Program](as400program-class.html) parameter list (via [AppendParm](as400program-class-append-parm-method.html) or [ AppendParms](as400program-class-append-parms-method.html)). Use the [ ObjectToParm](as400program-class-object-to_parm-method-main.html) and [SetParmsZeroValue](as400program-class-set-parms-zero-value-method.html) methods to set the value *data* of the **ProgParm** .
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

