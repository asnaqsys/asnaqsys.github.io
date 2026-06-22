---
title: "FieldType.NewInteger Method"
description: "Creates a new FieldType instance representing an integer field."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new FieldType instance representing an integer field.

<a id="fieldtype-newinteger-int-length"></a>
## FieldType NewInteger(int length)

Creates a new FieldType instance representing an integer field.

```cs
FieldType NewInteger(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the integer field. It should be either 2, 4, or 8.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

## See Also
- [FieldType class](field-type.html)
