---
title: "FieldType.NewPacked Method"
description: "Creates a new FieldType instance representing a packed decimal field."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new FieldType instance representing a packed decimal field.

<a id="fieldtype-newpacked-int-prec-int-scale"></a>
## FieldType NewPacked(int prec, int scale)

Creates a new FieldType instance representing a packed decimal field.

```cs
FieldType NewPacked(int prec, int scale)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | prec | The total number of digits in the packed decimal field.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | scale | The number of digits to the right of the decimal point in the packed decimal field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

## See Also
- [FieldType class](field-type.html)
