---
title: "IDSCallParm interface         | QSYS API Reference Guide"
description: "This interface should be implemented by any DataStructure class if an object of its type will be passed as a parameter to a program in the IBMi. "
last_modified_at: 2024-08-08T21:41:46Z
---

This interface should be implemented by any DataStructure class if an object of its type will be passed as a parameter to a program in the IBMi.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IDS](/reference/runtime/qsys-runtime/ids.html) | IDS | Gets the Data Structure |

## Methods

| Signature | Description |
| --- | --- |
| [GetProgParm](#progparm-getprogparmdatadirection-direction)([DataDirection](/reference/datagate/datagate-common/data-direction.html)) | Returns a ProgParm for a DS required by a Call to an external IBMi program.
| [GetProgParm](#progparm-getprogparmdatadirection-direction-int-modsdimensions)([DataDirection](/reference/datagate/datagate-common/data-direction.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a ProgParm for a MODS required by a Call to an external IBMi program.

### ProgParm GetProgParm([DataDirection direction](/reference/datagate/datagate-common/data-direction.html))

Returns a ProgParm for a DS required by a Call to an external IBMi program.

```cs
ProgParm GetProgParm(DataDirection direction)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | The DataDirection value that indicates whether the parameter is Input, Output, or Both.

#### Returns

| Type | Description
| --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | A ProgParm used in CALL.

### ProgParm GetProgParm([DataDirection direction](/reference/datagate/datagate-common/data-direction.html), [int modsDimensions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a ProgParm for a MODS required by a Call to an external IBMi program.

```cs
ProgParm GetProgParm(DataDirection direction, int modsDimensions)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | Direction of the data.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | modsDimensions | Size of the MODS.

#### Returns

| Type | Description
| --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | A ProgParm used in CALL.
