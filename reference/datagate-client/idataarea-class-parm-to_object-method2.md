---
title: IDataArea.ParmToObject(ASNA.DataGate.DataLink.ProgParm, System.Type, integer)

---

Returns an object of a specific type from the program parameter list provided with the program parameter object in the parameter list to get the value of, the type of the object returned by the method, and a zero-relative index identifying the element of the array to get the value of.

```cs
 public object ParmToObject(
[ASNA.DataGate.Client](DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a> Parameter,
   System.Type ReturnType,
   int Element
);
```


## Parameters



 *Parameter* 

: <a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a>.  
						The program parameter object in the parameter list to get the value of.

 *ReturnType* 

        <dt />
: 			System.Type.  The requested type of the object returned by the method. 

 *Element* 

: 					Integer. For paths including multiple-occurrence parameters, a zero-relative 
											index identifying the element of the array to get the value of. 


## Requirements

**Namespace:** <a href="dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IDataArea Class](idataarea-class.html)
      <br />
[IDataArea Class Members](dcsIDataAreaMembers.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

