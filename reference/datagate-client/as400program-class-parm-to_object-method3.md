---
title: As400Program.ParmToObject(ProgParm, System.Type)

---

Returns an object of a specific type from the program parameter list.

```cs
 public object ParmToObject(
ASNA.DataGate.DataLink.ProgParm Parameter
   Type ReturnType
);
```


## Parameters



 *Parameter* 

: 
[ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html).  The 
						program parameter object in the parameter list to get the value of. 

 *ReturnType*  
							</dt>
: System.Type.  The requested type of the object returned by the method.
							


## Returns

System.Object whose actual type is *ReturnType* .
## Exceptions

**ArgumentException** . Thrown if *Parameter* is a complex parameter (constructed with an instance of [ StructureType](structure-type-class.html)).

**InvalidOperationException** . Indicates that the **Connection** property of **As400Program** has not been set.
## Remarks

This form of **ParmToObject** may be used to get the value of simple parameters (non-structured) with a reference to the **ProgParm** object. *Parameter* should be a member of the **As400Program’s** parameter list. The value being referenced by this method should not belong to a multiple-occurrence type source, since there is no provision for specifying the index. The [ Connection](as400program-class-connection-property.html) property must be set (or the **As400Program** constructed with an [AdgConnection](adg-connection-class.html) object) prior to calling **ParmToObject** .

For the method to succeed, the type specified by *ReturnType* must have a valid conversion from the underlying parameter type. For example, a parameter for a decimal number can be converted to an arbitrary object type (such as a string), only if the object implements **System.IConvertible** and the **ChangeType** method yields a valid conversion. Most fundamental types in the System namespace implement IConvertible.
## Examples


```cs 
  /* Here, Prog is an initialized As400Program object,
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[3];
  Parms[0] = new ProgParm( new ProgParmType("CustName", 0, FieldType.NewChar(40)),
  DataDirection.Output);
  Parms[1] = new ProgParm( new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)),
  DataDirection.Output);
  Parms[2] = new ProgParm( new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
  DataDirection.Input);
   prog.AppendParms(Parms);
   prog.ObjectToParm(Parms[2], Quit400App, 0);
   prog.Execute(); 
  /* After calling the last two values in the parameter list
   * will have new values in it. To read them, we set our local
   * variables to the returned values in the parameters list. */
  CustName = Convert.ToString( prog.ParmToObject(System.Type.GetType("System.String"), "CustName", 0));
  TimeOfDay = Convert.ToDecimal( prog.ParmToObject(System.Type.GetType("System.Decimal"), "TimeOfDay", 0));
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
[Connection Property](as400program-class-connection-property.html)
      <br />
[AdgConnection Class](adg-connection-class.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)
      <br />
[ASNA.DataGate.DataLink.ProgParm Class](prog-parm-class.html)
      <br />
[ASNA.DataGate.DataLink.StructureType Class](structure-type-class.html)

