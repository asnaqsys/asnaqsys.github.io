---
title: As400Program.ParmToObject(System.Type, string, integer[])

---

Returns an object of a specific type from the program parameter list.

```cs
 public object ParmToObject(
   Type ReturnType,
   string ParameterName,
   int[] ElementIndices
);
```


## Parameters



 *ReturnType* 

: System.Type.  The requested type of the object returned by the method. 

 *ParameterName* 

: The name or path of the program parameter object in the parameter list. 

 *ElementIndices* 

: For paths including multiple-occurrence parameters only, the indices in the 
										path to the parameter.


## Exceptions

<span> **ArgumentException** .</span> Indicates that *ParameterName* , and if necessary *ElementIndices* , do not reference a valid parameter in the parameter list.

<span> **InvalidOperationException** .</span> Indicates that the **Connection** property of **As400Program** has not been set.
## Remarks

This form of **ParmToObject** may be used to get the value of both simple and structured parameters, using the optional parameter naming scheme allowed by [ProgParmType](prog-parm-type-class.html) and [StructureType](structure-type-class.html). The constructor for these classes allows the program parameters they represent to be given a string identifier. This identifier may have significance to the application, but it also may be used by this **ParmToObject** method to identify and retrieve the parameter after it has been added to the [As400Program](as400program-class.html) parameter list.

For simple parameters (constructed with **ProgParmType** ), *ParameterName* refers to the name given to the [ ProgParmType’s constructor](prog-parm-type-class-prog-parm-type-constructor.html). *ElementIndices* is ignored unless the simple parameter is a multiple-occurrence (single-dimension array) parameter. In this case, *ElementIndices* should be an integer array of at least one element. The first element in indices must be a zero-relative number identifying the element in the array to be returned by **ParmToObject** .

For complex parameters (constructed with [ StructureType's constructor](structure-type-class.html)), *ParameterName* refers to a path to a particular member of the data structure. This name should be in the form of string tokens separated by the character ‘.’, as in "x.y.z". Each token to the left of ‘.’ is the name of a structure containing a member named on the right of ‘.’. The leftmost string token refers to the name of the outermost structure or the [ProgParm](prog-parm-class.html) object contained in the **As400Program** parameter list. The rightmost token must refer to the name of a simple parameter type (constructed with <span> **ProgParmType** </span>) which is the member whose value is to be returned.

If the complex parameter path includes data types defined as multiple-occurrence types, then *ElementIndices* must contain an array of integers. The elements of indices refer to positions in the multiple occurrence types. For example, suppose a parameter consists of a multiple occurrence data structure, and one of the data structure’s members is a multiple occurrence character field type. To access the value of one of the character fields, *ElementIndices* must be an array of at least length 2. The first element of the array would reference an occurrence of the outer structure, and the second element of the array would refer to the particular character field to set.

If no multiple occurrence types are included in the path given by *ParameterName* , *ElementIndices* may be specified as an integer array of length zero.

The outermost <span> **ProgParm** </span> object identified by *ParameterName* and *ElementIndices* should be a member of the **As400Program’s** parameter list. The [Connection](as400program-class-connection-property.html) property must be set (or the **As400Program** constructed with an [AdgConnection](adg-connection-class.html) object) prior to calling <span> **ParmToObject** </span>.

For the method to succeed, the type specified by *ReturnType* must have a valid conversion to the underlying parameter type. For example, a parameter for a decimal number can be returned as an arbitrary object (such as a string), only if the object implements <span> **System.IConvertible** </span>, and the <span> **ChangeType** </span> method yields a valid conversion. Most fundamental types in the System namespace implement <span>IConvertible</span>.
## Examples


```cs 
  /* Here, Prog is an initialized As400Program object, 
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
  TimeOfDay = Convert.ToDecimal(
        prog.ParmToObject(System.Type.GetType("System.Decimal"),
        "TimeOfDay",
        0));
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
[ASNA.DataGate.DataLink.ProgParmType Class](prog-parm-type-class.html)
      <br />
[ProgParmType Constructor](prog-parm-type-class-prog-parm-type-constructor.html)
      <br />
[ASNA.DataGate.DataLink.StructureType Class](structure-type-class.html)
      <br />
      [StructureType 
					Constructor](structure-type-class.html)
      <br />
[ASNA.DataGate.DataLink.ProgParm Class](prog-parm-class.html)

