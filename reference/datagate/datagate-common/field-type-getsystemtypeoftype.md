---
title: "FieldType.GetSystemTypeOfType Method"
description: "Gets the corresponding .NET type for a given DataTypes value and byte length."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the corresponding .NET type for a given DataTypes value and byte length.

<a id="type-getsystemtypeoftype-datatypes-dt-int-bytelength"></a>
## Type GetSystemTypeOfType(DataTypes dt, int byteLength)

Gets the corresponding .NET type for a given DataTypes value and byte length.

```cs
Type GetSystemTypeOfType(DataTypes dt, int byteLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataTypes](/reference/datagate/datagate-common/data-types.html) | dt | The DataTypes value to get the .NET type for.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | byteLength | The byte length of the data type.

#### Returns

| Type | Description
| --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | The corresponding .NET type, or null if no match is found.

## See Also
- [FieldType class](field-type.html)
