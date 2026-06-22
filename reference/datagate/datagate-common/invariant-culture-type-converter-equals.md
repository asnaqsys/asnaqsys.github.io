---
title: "InvariantCultureTypeConverter.Equals Method"
description: "Determines whether the specified object is equal to the current object, using the wrapped converter's Equals method."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the specified object is equal to the current object, using the wrapped converter's Equals method.

<a id="bool-equals-object-obj"></a>
## bool Equals(object obj)

Determines whether the specified object is equal to the current object, using the wrapped converter's Equals method.

#### Remarks
This method overrides the base implementation to ensure that the equality check is performed using the wrapped converter's Equals method.This is useful when you need to ensure that equality checks are not affected by the current culture settings of the system.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The  to compare with the current object.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the specified object is equal to the current object.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
