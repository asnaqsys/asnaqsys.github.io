---
title: "ILayout interface             | QSYS API Reference Guide"
description: "Defines operations for objects describing fields in a data structure. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines operations for objects describing fields in a data structure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ArrayLength | If the layout describes an array, the number of elements in the array. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Decimals | If the layout describes a fixed decimal number, the number of decimal positions. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Digits | If the layout describes a fixed decimal number, the number of digits. |
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | Format | For date/time/timestamps, the enum value representing the format of the data. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsArray | True if this layout describes an array, false otherwise. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ItemLength | For arrays, the length on an array element. For scalars, this is the same as Length. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the field described by the layout. If the layout describes an array, the total length of all elements of the array. |
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | Separator | For date/time/timestamps, the enum value representing the data separator. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Skip | For OVERLAY arrays, the number of positions to skip between array elements. |
| [LayoutType](/reference/runtime/qsys-runtime/layout-type.html) | Type | Gets an enum value that represents the type of the field. |

## Methods

| Signature | Description |
| --- | --- |
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Equality comparer.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Equality comparer.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object against which to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the ILayouts are equivalent, i.e. if all of their properties correspondingly have the same values.
