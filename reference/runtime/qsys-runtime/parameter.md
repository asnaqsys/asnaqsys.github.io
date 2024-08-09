---
title: "Parameter class               | QSYS API Reference Guide"
description: "Describes a parameter sent into an IBMi program call. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes a parameter sent into an IBMi program call.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Parameter](#parameterstring-fieldtype-datadirection-object)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](/reference/datagate/datagate-common/field-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Create a Parm object to represent an IBMi program parameter.

### Parameter([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](/reference/datagate/datagate-common/field-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Create a Parm object to represent an IBMi program parameter.

```cs
Parameter(String, FieldType, DataDirection, Object)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [FieldType](/reference/datagate/datagate-common/field-type.html) | type | The FieldType of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | The DataDirection of the parameter.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The value of the parameter.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | Direction | Specifies if the parameter will be input, output, or update (both). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Name of the parameter. |
| [FieldType](/reference/datagate/datagate-common/field-type.html) | Type | Describes the type and size of the parameter. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | The value of the parameter. |
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueArray | The value of the parameter array. |
