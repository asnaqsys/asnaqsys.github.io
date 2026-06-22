---
title: "FieldType.NewBinary Method"
description: "Creates a new FieldType instance representing a binary field."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new FieldType instance representing a binary field.

<a id="fieldtype-newbinary-int-prec-int-scale"></a>
## FieldType NewBinary(int prec, int scale)

Creates a new FieldType instance representing a binary field.

```cs
FieldType NewBinary(int prec, int scale)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | prec | The total number of digits in the binary field.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | scale | The number of digits to the right of the decimal point in the binary field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

## See Also
- [FieldType class](field-type.html)
