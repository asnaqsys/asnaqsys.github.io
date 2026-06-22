---
title: "FieldType.NewDBCS Method"
description: "Creates a new FieldType instance representing a DBCS field."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new FieldType instance representing a DBCS field.

<a id="fieldtype-newdbcs-int-length-dbcsformat-fmt"></a>
## FieldType NewDBCS(int length, DbcsFormat fmt)

Creates a new FieldType instance representing a DBCS field.

```cs
FieldType NewDBCS(int length, DbcsFormat fmt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the DBCS field.
| [DbcsFormat](/reference/datagate/datagate-common/dbcs-format.html) | fmt | The format of the DBCS field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

## See Also
- [FieldType class](field-type.html)
