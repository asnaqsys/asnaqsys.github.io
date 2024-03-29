---
title: As400Program.ObjectToParm(ProgParm, object)

---

Converts an object or value type to a parameter list value.

```cs
 public void ObjectToParm(
   ProgParm Parameter,
   object Value
);
```


## Parameters



          <span> *Parameter* 
          </span>

: 
[ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html).  The 
						value to be set.

 *Value* 

: The name of the program parameter object in the parameter list.
							


## Exceptions

**ArgumentException** . Thrown if *parameter* is a complex parameter (constructed with an instance of [StructureType](structure-type-class.html)).

**InvalidOperationException** . Indicates that the [ Connection](as400program-class-connection-property.html) property of **As400Program** has not been set.
## Remarks

This form of **ObjectToParm** may be used to set the value of simple parameters (non-structured) with a reference to the **ProgParm** object. The object should be a member of the [ As400Program's](as400program-class.html) parameter list. The **Connection** property must be set (or the **As400Program** constructed with an [AdgConnection](adg-connection-class.html) object) prior to calling **ObjectToParm** .

For the method to succeed, the *Value* object must have a valid conversion to the underlying parameter type. For example, a parameter for a decimal number can be set with an arbitrary object (such as a string), only if the object implements **System.IConvertible** and the **ToDecimal** method yields a valid conversion. Most fundamental types in the System namespace implement IConvertible.

This method of **ObjectToParm** should not be used if *Parameter* is a "multiple-occurrence" parameter type. Instead, use a method that allows the index of the multiple-occurrence parameter to be specified.
## Examples


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

