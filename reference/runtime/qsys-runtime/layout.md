---
title: "Layout struct                 | QSYS API Reference Guide"
description: "Defines a layout for a field in a data structure. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines a layout for a field in a data structure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

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
| [Binary](#ilayout-binaryint-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDecimal field with a binary format.
| [BinaryArray](#ilayout-binaryarrayint-arraylength-int-digits-int-decimals-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDecimal array field with binary format.
| [Byte()](#ilayout-byte) | Creates a layout for a byte field.
| [ByteArray](#ilayout-bytearrayint-arraylength-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a byte array field.
| [Char()](#ilayout-char) | Creates a layout for a char field.
| [CharArray](#ilayout-chararrayint-arraylength-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a character array field.
| [Date](#ilayout-datedatetimeformat-format-datetimeseparator-separator)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Creates a layout for a FixedDate field.
| [DateArray](#ilayout-datearrayint-arraylength-datetimeformat-format-datetimeseparator-separator-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDate array field.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Equality comparer.
| [FixedString](#ilayout-fixedstringint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedString field.
| [FixedStringArray](#ilayout-fixedstringarrayint-arraylength-int-length-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedString array field.
| [GetHashCode()](#int-gethashcode) | Get the unique hashcode of this instance.
| [Hex](#ilayout-hexint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a Hex (byte[]) field.
| [Indicator()](#ilayout-indicator) | Creates a layout for an Indicator field.
| [IndicatorArray](#ilayout-indicatorarrayint-arraylength-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for an Indicator array field.
| [Integer()](#ilayout-integer) | Creates a layout for an integer field.
| [IntegerArray](#ilayout-integerarrayint-arraylength-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for an int array field.
| [Long()](#ilayout-long) | Creates a layout for a long field.
| [LongArray](#ilayout-longarrayint-arraylength-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a long array field.
| [NewLayout](#ilayout-newlayoutlayouttype-type-int-digits-int-decimals-int-length-datetimeformat-format-datetimeseparator-separator-int-arraylength-int-skip)([LayoutType](/reference/runtime/qsys-runtime/layout-type.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout with the given values.
| [op_Equality](#bool-op-equalitylayout-first-layout-second)([Layout](/reference/runtime/qsys-runtime/layout.html), [Layout](/reference/runtime/qsys-runtime/layout.html)) | Equality operator.
| [op_Inequality](#bool-op-inequalitylayout-first-layout-second)([Layout](/reference/runtime/qsys-runtime/layout.html), [Layout](/reference/runtime/qsys-runtime/layout.html)) | Inequality operator.
| [Packed](#ilayout-packedint-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDecimal field with a packed format.
| [PackedArray](#ilayout-packedarrayint-arraylength-int-digits-int-decimals-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDecimal array field with packed format.
| [Short()](#ilayout-short) | Creates a layout for a short field.
| [ShortArray](#ilayout-shortarrayint-arraylength-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a short array field.
| [Time](#ilayout-timedatetimeformat-format-datetimeseparator-separator)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Creates a layout for a FixedTime field.
| [TimeArray](#ilayout-timearrayint-arraylength-datetimeformat-format-datetimeseparator-separator-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedTime array field.
| [Timestamp](#ilayout-timestampdatetimeseparator-separator)([DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Creates a layout for a FixedTimestamp field.
| [TimestampArray](#ilayout-timestamparrayint-arraylength-datetimeseparator-separator-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedTimestamp array field.
| [Zoned](#ilayout-zonedint-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDecimal field with a zoned format.
| [ZonedArray](#ilayout-zonedarrayint-arraylength-int-digits-int-decimals-int-skip)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a layout for a FixedDecimal array field with zoned format.

### ILayout Binary([int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDecimal field with a binary format.

```cs
ILayout Binary(int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in this FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in this FixedDecimal.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDecimal field with a binary format.

### ILayout BinaryArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDecimal array field with binary format.

```cs
ILayout BinaryArray(int arrayLength, int digits, int decimals, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDecimal array field with binary format.

### ILayout Byte()

Creates a layout for a byte field.

```cs
ILayout Byte()
```

### ILayout ByteArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a byte array field.

```cs
ILayout ByteArray(int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a byte array field.

### ILayout Char()

Creates a layout for a char field.

```cs
ILayout Char()
```

### ILayout CharArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a character array field.

```cs
ILayout CharArray(int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a character array field.

### ILayout Date([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Creates a layout for a FixedDate field.

```cs
ILayout Date(DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The enum value describing the format of this FixedDate.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The enum value describing the separator this FixedDate uses.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDate field with the given format and separator.

### ILayout DateArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDate array field.

```cs
ILayout DateArray(int arrayLength, DateTimeFormat format, DateTimeSeparator separator, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The enum value describing the format of this FixedDate.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The enum value describing the separator this FixedDate uses.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDate array field.

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
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the Layouts are equivalent, i.e. if all of their properties correspondingly have the same values.

### ILayout FixedString([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedString field.

```cs
ILayout FixedString(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the FixedString field.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedString field.

### ILayout FixedStringArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedString array field.

```cs
ILayout FixedStringArray(int arrayLength, int length, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length of the FixedStrings
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedString array field.

### int GetHashCode()

Get the unique hashcode of this instance.

```cs
int GetHashCode()
```

### ILayout Hex([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a Hex (byte[]) field.

```cs
ILayout Hex(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the Hex field.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a Hex field.

### ILayout Indicator()

Creates a layout for an Indicator field.

```cs
ILayout Indicator()
```

### ILayout IndicatorArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for an Indicator array field.

```cs
ILayout IndicatorArray(int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing an Indicator array field.

### ILayout Integer()

Creates a layout for an integer field.

```cs
ILayout Integer()
```

### ILayout IntegerArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for an int array field.

```cs
ILayout IntegerArray(int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing an int array field.

### ILayout Long()

Creates a layout for a long field.

```cs
ILayout Long()
```

### ILayout LongArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a long array field.

```cs
ILayout LongArray(int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a long array field.

### ILayout NewLayout([LayoutType type](/reference/runtime/qsys-runtime/layout-type.html), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html), [int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout with the given values.

```cs
ILayout NewLayout(LayoutType type, int digits, int decimals, int length, DateTimeFormat format, DateTimeSeparator separator, int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [LayoutType](/reference/runtime/qsys-runtime/layout-type.html) | type | LayoutType of this layout
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | If the layout is numeric, the number of digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | If the layout is decimal numeric, the number of decimal positions.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | For FixedString and Hex, length of the field.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | For Date and Time, the date or time format.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | For Date, Time and Timestamp, the separator.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | For arrays, the size of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | For non-contiguous array, the number of positions to skip between elements.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The new layout.

### bool op_Equality([Layout first](/reference/runtime/qsys-runtime/layout.html), [Layout second](/reference/runtime/qsys-runtime/layout.html))

Equality operator.

```cs
bool op_Equality(Layout first, Layout second)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Layout](/reference/runtime/qsys-runtime/layout.html) | first | The first Layout to compare.
| [Layout](/reference/runtime/qsys-runtime/layout.html) | second | The second Layout to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the Layouts are equivalent, i.e. if all of their properties correspondingly have the same values.

### bool op_Inequality([Layout first](/reference/runtime/qsys-runtime/layout.html), [Layout second](/reference/runtime/qsys-runtime/layout.html))

Inequality operator.

```cs
bool op_Inequality(Layout first, Layout second)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Layout](/reference/runtime/qsys-runtime/layout.html) | first | The first Layout to compare.
| [Layout](/reference/runtime/qsys-runtime/layout.html) | second | The second Layout to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the Layouts are different, i.e. if any of their properties correspondingly have different values.

### ILayout Packed([int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDecimal field with a packed format.

```cs
ILayout Packed(int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in this FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in this FixedDecimal.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDecimal field with a packed format.

### ILayout PackedArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDecimal array field with packed format.

```cs
ILayout PackedArray(int arrayLength, int digits, int decimals, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDecimal array field with packed format.

### ILayout Short()

Creates a layout for a short field.

```cs
ILayout Short()
```

### ILayout ShortArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a short array field.

```cs
ILayout ShortArray(int arrayLength, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a short array field.

### ILayout Time([DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Creates a layout for a FixedTime field.

```cs
ILayout Time(DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The enum value describing the format of this FixedTime.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The enum value describing the separator this FixedTime uses.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedTime field with the given format and separator.

### ILayout TimeArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedTime array field.

```cs
ILayout TimeArray(int arrayLength, DateTimeFormat format, DateTimeSeparator separator, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The enum value describing the format of this FixedTime.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The enum value describing the separator this FixedTime uses.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedTime array field.

### ILayout Timestamp([DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Creates a layout for a FixedTimestamp field.

```cs
ILayout Timestamp(DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The enum value describing the separator this FixedTimestamp uses.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedTimestamp field with the given separator.

### ILayout TimestampArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedTimestamp array field.

```cs
ILayout TimestampArray(int arrayLength, DateTimeSeparator separator, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The enum value describing the separator this FixedTimestamp uses.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedTimestamp array field.

### ILayout Zoned([int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDecimal field with a zoned format.

```cs
ILayout Zoned(int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in this FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in this FixedDecimal.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDecimal field with a zoned format.

### ILayout ZonedArray([int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int skip](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a layout for a FixedDecimal array field with zoned format.

```cs
ILayout ZonedArray(int arrayLength, int digits, int decimals, int skip)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | Length (number of elements) of the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the FixedDecimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | skip | Number of positions to skip between elements in a non-contiguous array.

#### Returns

| Type | Description
| --- | ---
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | The layout describing a FixedDecimal array field with zoned format.
