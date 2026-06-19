---
title: "NewLineDelimeter.Equals Method"
description: "Determines whether the specified object is equal to the current object."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the specified object is equal to the current object.

<a id="bool-equals-object-obj"></a>
## bool Equals(object obj)

Determines whether the specified object is equal to the current  object.

#### Remarks
This method overrides the base  method and performs a check to determine equality:- If the provided object is a  instance, it returns true.- If the provided object is not a  instance, it calls the base  method to compare the two objects.

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
- [NewLineDelimeter class](new-line-delimeter.html)
