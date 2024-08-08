---
title: "IFixedArrayInDS<T1, T2> interface"
description: "Describes minimum operations for a fixed size array contained in a DataStructure. "
last_modified_at: 2024-08-08T21:41:46Z
---

Describes minimum operations for a fixed size array contained in a DataStructure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ParentDS | The container DataStructure. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SkipPositions | If the array is non-contiguous in the DataStructure buffer, the number of positions between two consecutive elements of the array. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StartPosition | The starting position of the array within the DataStructure buffer. |

## Methods

| Signature | Description |
| --- | --- |
| [GetStartingPosition](#int-getstartingpositionint-index)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.

### int GetStartingPosition([int index](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the starting position in the DataStructure buffer of the element indicated by the index parameter.

```cs
int GetStartingPosition(int index)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | index | The index of the desired element position.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The position in the buffer of the element at index.
