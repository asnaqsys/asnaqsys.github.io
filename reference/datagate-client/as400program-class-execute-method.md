---
title: As400Program.Execute Method

TocParent: dcsAs400ProgramMethodsMain

---

Runs the database program.

```cs
 public void Execute();
```


## Exceptions

<br />



| Exception Type | Condition |
| ---- | ---- |
| InvalidOperationException | The [ProgramPath](as400program-class-program-path-property.html) property has not been set or contains a zero-length string. |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of 							<br /> 							dgException.Error | Condition |
| ---- | ---- |
| dgEpMEMEXCEPTION | An IBM i memory exception occurred (an exception in the MCH36xx series). Generally this indicates a bad pointer in the called program. Examine the job log for details. |
| dgEpPGMNOTFND | The value specified for the **ProgramPath** property does not refer to a valid program object. |
| dgEINVARG | The value specified for the **ProgramPath** property is not a valid database object path (did you forget a library name or *LIBL?). |
| dgEpPGMERR | The number of parameters in the parameter list exceeds the maximum allowed by DataGate. Currently the maximum is 36. |
| dgEsAS400ERROR | The IBM i server encountered a system error. Details may be available via the [ SystemError](dgexception-class-system-error-field.html) and [Text](disconnectingfroma-database.html) fields of dgException. |



## Remarks

The **Execute** method invokes the program on the database server. If the program requires parameters, they should be added to the parameter list (with [AppendParm Method](as400program-class-append-parm-method.html) and [AppendParms](as400program-class-append-parms-method.html)) prior to calling **Execute** . If any parameters are "input" parameters, their value should be set (with [ ObjectToParm](as400program-class-object-to_parm-method-main.html)) first. The [ Connection](as400program-class-connection-property.html) and [ProgramPath](as400program-class-program-path-property.html) properties must be set (directly or by [ As400Program constructor](as400program-class-as400program-method-main.html)) prior to calling **Execute** .

The name of the program, as specified by the **ProgramPath** property, is validated by this method. If a program cannot be found at the specified location, dgException is raised with the [ Error](dgexception-class-error-field.html) property set to dgEpPGMNOTFND.

If an i Series system exception occurs in the called program, dgException is raised with the Error property set to dgEsAS400ERROR. System details of the exception will be available in the **Text** , **SystemError** , and [ErrorClass](dgexception-class-error-class-field.html) fields of dgException.

Upon successful return from **Execute** , the values of any "output" parameters passed to the program will be available with the [ ParmToObject](as400program-class-parm-to_object-method-main.html) method.

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


## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[As400Program Class](as400program-class.html)
      <br />
[As400Program Class Members](as400program-members.html)
      <br />
[AppendParm Method](as400program-class-append-parm-method.html)
      <br />
[AppendParms Method](as400program-class-append-parms-method.html)
      <br />
[Connection Property](as400program-class-connection-property.html)
      <br />
      [As400ProgramClass 
					Constructors](as400program-class-as400program-method-main.html)
      <br />
[ObjectToParm Method](as400program-class-object-to_parm-method-main.html)
      <br />
[ParmToObject Method](as400program-class-parm-to_object-method-main.html)
      <br />
[ProgramPath Property](as400program-class-program-path-property.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

