---
title: "IFixedArrayBase<T1, T2> interface"
description: "Base interface for all fixed sized arrays in the fixed-sized type framework. These arrays are unidimensional. "
last_modified_at: 2024-08-09T16:18:25Z
---

Base interface for all fixed sized arrays in the fixed-sized type framework. These arrays are unidimensional.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [TType](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Item | Indexer over the array, gets or sets the element at that position. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Returns the length of the array. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears all elements of the array to their default value.
| [CopyFrom](#void-copyfromttype--sourcearray-int-targetstartat)([TType\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copies elements of a .Net array of the same element type into this fixed sized array.

### void Clear()

Clears all elements of the array to their default value.

```cs
void Clear()
```

### void CopyFrom([TType\[\] sourceArray](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copies elements of a .Net array of the same element type into this fixed sized array.

```cs
void CopyFrom(TType[] sourceArray, int targetStartAt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TType\[\]](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | sourceArray | The array to copy from.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | The index in this array where the copying should start.
