---
title: "Delimiter.Equals Method"
description: "Determines whether the specified object is equal to the current object."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the specified object is equal to the current object.

<a id="bool-equals-object-obj"></a>
## bool Equals(object obj)

Determines whether the specified object is equal to the current object.

#### Remarks
This method overrides the base  method and performs a series of checks to determine equality:- If the provided object is a  instance, it uses the equality operator (==) to compare the two instances.- If the provided object is a , it creates a new  instance from the character and uses the equality operator to compare the two instances.- If the provided object is neither a  nor a , it returns false.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current object.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is equal to the current object; otherwise, false.

## See Also
- [Delimiter class](delimiter.html)
