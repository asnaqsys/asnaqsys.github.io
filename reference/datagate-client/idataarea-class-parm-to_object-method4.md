---
title: IDataArea.ParmToObject(System.Type, string, integer[])

---

Returns an object of a specific type from the program parameter list provided with the type of the object returned by the method, the name or path of the program parameter object in the parameter list, and the indices in the path to the parameter.

```cs
 public object ParmToObject(
   System.Type ReturnType,
   string ParameterName,
   int[] ElementIndices
);
```


## Parameters



 *ReturnType* 

        <dt />
: 	System.Type.  The requested type of the object returned by the method. 

 *ParameterName* 

: 			The name or path of the program data area. 

 *ElementIndices* 

: 					Integer. For paths including multiple-occurrence parameters, the indices in the 
											path to the data area. 


## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IDataArea Class](idataarea-class.html)
      <br />
[IDataArea Class Members](dcsIDataAreaMembers.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

