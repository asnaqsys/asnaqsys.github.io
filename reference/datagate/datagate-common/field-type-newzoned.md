---
title: "FieldType.NewZoned Method"
description: "Creates a new FieldType instance representing a zoned decimal field."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new FieldType instance representing a zoned decimal field.

<a id="fieldtype-newzoned-int-prec-int-scale"></a>
## FieldType NewZoned(int prec, int scale)

Creates a new FieldType instance representing a zoned decimal field.

```cs
FieldType NewZoned(int prec, int scale)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | prec | The total number of digits in the zoned decimal field.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | scale | The number of digits to the right of the decimal point in the zoned decimal field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

## See Also
- [FieldType class](field-type.html)
