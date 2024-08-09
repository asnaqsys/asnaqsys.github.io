---
title: "DataStructure class           | QSYS API Reference Guide"
description: "Contains the functionality to support the semantics of a RPG Data Structure with a memory layout. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains the functionality to support the semantics of a RPG Data Structure with a memory layout.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DataStructure](#datastructureint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructs a Data Structure object with a buffer of the given size.
| [DataStructure](#datastructureilayout)([ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html)) | Constructs a Data Structure object given an array of layout-described fields. The Data Structure size is computed out of the sizes of the individual fields.

### DataStructure([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructs a Data Structure object with a buffer of the given size.

```cs
DataStructure(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | size | Size of the Data Structure buffer.

### DataStructure([ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html))

Constructs a Data Structure object given an array of layout-described fields. The Data Structure size is computed out of the sizes of the individual fields.

```cs
DataStructure(ILayout[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ILayout\[\]](/reference/runtime/qsys-runtime/i-layout.html) | layouts | An ILayout array of field descriptions, assumed to be consecutive in the Data Structure.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | BufferDescription | Returns the flat description of the data structure buffer. |
| [DSDataArea](/reference/runtime/qsys-runtime/ds-data-area.html) | DataArea | Gets a DSDataArea object for this Data Structure. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DSName | Gets the name of this Data Structure object. |
| [List\<IDSField\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | Fields | Gets the description of the Fields in this Data Structure. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Length of the Data Structure buffer. |

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Clears the Data Structure. If the layout is defined, each field is cleared to its default value. Otherwise it is cleared to blanks.
| [Dump()](#string-dump) | Gets the contents of the Data Structure buffer as a string value.
| [GetBinary](#decimal-getbinaryint-start-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a decimal number stored as a Binary decimal number starting at the specified position in the Data Structure buffer.
| [GetByte](#byte-getbyteint-position)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a byte value from the specified position in the Data Structure buffer.
| [GetChar](#char-getcharint-position)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a character from the specified position in the Data Structure buffer.
| [GetDate](#datetime-getdateint-start-datetimeformat-format-datetimeseparator-separator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Gets a Date value stored with the specified format and date separator at the specified starting position in the Data Structure buffer.
| [GetHex](#byte--gethexint-start-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a byte array from the Data Structure buffer, at the given start position for the given length.
| [GetIndicator](#char-getindicatorint-position)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a character from the specified position in the Data Structure buffer and returns either '0', if the character is '0', or '1'if the character is anything else.
| [GetInteger](#int-getintegerint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets an integer (Int32) value starting at the specified position in the Data Structure buffer.
| [GetLong](#long-getlongint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets an long (Int64) value starting at the specified position in the Data Structure buffer.
| [GetNullableBinary](#nullable-decimal-getnullablebinaryint-start-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a decimal number stored as a Binary decimal number starting at the specified position in the Data Structure buffer.
| [GetNullableByte](#nullable-byte-getnullablebyteint-position)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a byte value from the specified position in the Data Structure buffer.
| [GetNullableChar](#nullable-char-getnullablecharint-position)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a character from the specified position in the Data Structure buffer.
| [GetNullableDate](#nullable-datetime-getnullabledateint-start-datetimeformat-format-datetimeseparator-separator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Gets a Date value stored with the specified format and date separator at the specified starting position in the Data Structure buffer.
| [GetNullableIndicator](#nullable-char-getnullableindicatorint-position)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a character from the specified position in the Data Structure buffer and returns either '0', if the character is '0', or '1'if the character is anything else.
| [GetNullableInteger](#nullable-int-getnullableintegerint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets an integer (Int32) value starting at the specified position in the Data Structure buffer.
| [GetNullableLong](#nullable-long-getnullablelongint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets an long (Int64) value starting at the specified position in the Data Structure buffer.
| [GetNullablePacked](#nullable-decimal-getnullablepackedint-start-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a decimal number stored as a Packed decimal number starting at the specified position in the Data Structure buffer.
| [GetNullableShort](#nullable-short-getnullableshortint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a short (Int16) value starting at the specified position in the Data Structure buffer.
| [GetNullableString](#string-getnullablestringint-start-int-len)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a segment of the Data Structure buffer as a string.
| [GetNullableTime](#nullable-datetime-getnullabletimeint-start-datetimeformat-format-datetimeseparator-separator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Gets a Time value stored with the specified format and time separator at the specified starting position in the Data Structure buffer.
| [GetNullableTimestamp](#nullable-datetime-getnullabletimestampint-start-datetimeseparator-separator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Gets a Timestamp value stored with the specified timestamp separator at the specified starting position in the Data Structure buffer.
| [GetNullableZoned](#nullable-decimal-getnullablezonedint-start-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a decimal number stored as a Zoned decimal number starting at the specified position in the Data Structure buffer.
| [GetPacked](#decimal-getpackedint-start-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a decimal number stored as a Packed decimal number starting at the specified position in the Data Structure buffer.
| [GetShort](#short-getshortint-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a short (Int16) value starting at the specified position in the Data Structure buffer.
| [GetString](#string-getstringint-start-int-len)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a segment of the Data Structure buffer as a string.
| [GetTime](#datetime-gettimeint-start-datetimeformat-format-datetimeseparator-separator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Gets a Time value stored with the specified format and time separator at the specified starting position in the Data Structure buffer.
| [GetTimestamp](#datetime-gettimestampint-start-datetimeseparator-separator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Gets a Timestamp value stored with the specified timestamp separator at the specified starting position in the Data Structure buffer.
| [GetValue\<U\>](#u-getvalue-u-int-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the value of the field at the requested starting position in the buffer.
| [GetZoned](#decimal-getzonedint-start-int-digits-int-decimals)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a decimal number stored as a Zoned decimal number starting at the specified position in the Data Structure buffer.
| [Load](#void-loadstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the Data Structure buffer to the given string value, padding with blanks if necessary.
| [ObjectToParm](#void-objecttoparmas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ObjectToParm implementation. Converts the Data Structure field values into parameters for calling the given IBMi program.
| [op_Explicit](#string-op-explicitdatastructure-datastructure)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html)) | Casting operator to string. Returns the data structure as a string.
| [op_Implicit](#dsdataarea-op-implicitdatastructure-ds)([DataStructure](/reference/runtime/qsys-runtime/data-structure.html)) | Casting operator to DSDataArea.
| [ParmToObject](#void-parmtoobjectas400program-program-int32--indices-int-dim)([As400Program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | IDS.ParmToObject implementation. Gets the Data Structure field values returned from a call to an IBMi program.
| [SetBinary](#void-setbinarydecimal-value-int-start-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a decimal number as a Binary decimal number starting at the specified position in the Data Structure buffer.
| [SetByte](#void-setbytebyte-value-int-position)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a byte value in the specified position in the Data Structure buffer.
| [SetChar](#void-setcharchar-val-int-position)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a character value in the specified position in the Data Structure buffer.
| [SetDate](#void-setdatedatetime-value-int-start-datetimeformat-format-datetimeseparator-separator)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Stores the Date part of a DateTime value with the specified format and date separator in the Data Structure buffer.
| [SetHex](#void-sethexbyte--value-int-start-int-length)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a byte array in the Data Structure buffer, at the given start position for the given length.
| [SetIndicator](#void-setindicatorchar-val-int-position)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores an indicator value specified as a character in the specified position in the Data Structure buffer.
| [SetInteger](#void-setintegerint-value-int-start)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores an integer (Int32) value starting at the specified position in the Data Structure buffer.
| [SetLong](#void-setlonglong-value-int-start)([Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores an long (Int64) value starting at the specified position in the Data Structure buffer.
| [SetNullableBinary](#void-setnullablebinarynullable-decimal-value-int-start-int-digits-int-decimals)([Nullable\<Decimal\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a decimal number as a Binary decimal number starting at the specified position in the Data Structure buffer.
| [SetNullableByte](#void-setnullablebytenullable-byte-value-int-position)([Nullable\<Byte\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a byte value in the specified position in the Data Structure buffer.
| [SetNullableChar](#void-setnullablecharnullable-char-val-int-position)([Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a character value in the specified position in the Data Structure buffer.
| [SetNullableDate](#void-setnullabledatenullable-datetime-value-int-start-datetimeformat-format-datetimeseparator-separator)([Nullable\<DateTime\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Stores the Date part of a DateTime value with the specified format and date separator in the Data Structure buffer.
| [SetNullableIndicator](#void-setnullableindicatornullable-char-val-int-position)([Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores an indicator value specified as a character in the specified position in the Data Structure buffer.
| [SetNullableInteger](#void-setnullableintegernullable-int-value-int-start)([Nullable\<Int32\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores an integer (Int32) value starting at the specified position in the Data Structure buffer.
| [SetNullableLong](#void-setnullablelongnullable-long-value-int-start)([Nullable\<Int64\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores an long (Int64) value starting at the specified position in the Data Structure buffer.
| [SetNullablePacked](#void-setnullablepackednullable-decimal-value-int-start-int-digits-int-decimals)([Nullable\<Decimal\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a decimal number as a Packed decimal number starting at the specified position in the Data Structure buffer.
| [SetNullableShort](#void-setnullableshortnullable-short-value-int-start)([Nullable\<Int16\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a short (Int16) value starting at the specified position in the Data Structure buffer.
| [SetNullableString](#void-setnullablestringstring-val-int-start-int-len-char-padchar-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a string into a segment the Data Structure buffer, left adjusted. Pads on the right if necessary.
| [SetNullableStringR](#void-setnullablestringrstring-val-int-start-int-len-char-padchar-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a string into a segment the Data Structure buffer, right adjusted. Pads on the left if necessary.
| [SetNullableTime](#void-setnullabletimenullable-datetime-value-int-start-datetimeformat-format-datetimeseparator-separator)([Nullable\<DateTime\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Stores the Time part of a DateTime value with the specified format and time separator in the Data Structure buffer.
| [SetNullableTimestamp](#void-setnullabletimestampnullable-datetime-value-int-start-datetimeseparator-separator)([Nullable\<DateTime\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Stores the DateTime value as a Timestamp with the specified timestamp separator in the Data Structure buffer.
| [SetNullableZoned](#void-setnullablezonednullable-decimal-value-int-start-int-digits-int-decimals)([Nullable\<Decimal\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a decimal number as a Zoned decimal number starting at the specified position in the Data Structure buffer.
| [SetPacked](#void-setpackeddecimal-value-int-start-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a decimal number as a Packed decimal number starting at the specified position in the Data Structure buffer.
| [SetShort](#void-setshortshort-value-int-start)([Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a short (Int16) value starting at the specified position in the Data Structure buffer.
| [SetString](#void-setstringstring-val-int-start-int-len-char-padchar-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a string into a segment the Data Structure buffer, left adjusted. Pads on the right if necessary.
| [SetStringR](#void-setstringrstring-val-int-start-int-len-char-padchar-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a string into a segment the Data Structure buffer, right adjusted. Pads on the left if necessary.
| [SetTime](#void-settimedatetime-value-int-start-datetimeformat-format-datetimeseparator-separator)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Stores the Time part of a DateTime value with the specified format and time separator in the Data Structure buffer.
| [SetTimestamp](#void-settimestampdatetime-value-int-start-datetimeseparator-separator)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html)) | Stores the DateTime value as a Timestamp with the specified timestamp separator in the Data Structure buffer.
| [SetValue\<U\>](#void-setvalue-u-u-value-int-start)([U](https://learn.microsoft.com/en-us/dotnet/standard/generics), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the value of the field at the requested starting position in the buffer.
| [SetZoned](#void-setzoneddecimal-value-int-start-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Stores a decimal number as a Zoned decimal number starting at the specified position in the Data Structure buffer.
| [ToString()](#string-tostring) | Gets the contents of the data structure as a string.

### void Clear()

Clears the Data Structure. If the layout is defined, each field is cleared to its default value. Otherwise it is cleared to blanks.

```cs
void Clear()
```

### string Dump()

Gets the contents of the Data Structure buffer as a string value.

```cs
string Dump()
```

### decimal GetBinary([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a decimal number stored as a Binary decimal number starting at the specified position in the Data Structure buffer.

```cs
decimal GetBinary(int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Binary decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Binary decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number value of the Binary decimal number.

### byte GetByte([int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a byte value from the specified position in the Data Structure buffer.

```cs
byte GetByte(int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | The character at the given position in the buffer.

### char GetChar([int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a character from the specified position in the Data Structure buffer.

```cs
char GetChar(int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | The character at the given position in the buffer.

### DateTime GetDate([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Gets a Date value stored with the specified format and date separator at the specified starting position in the Data Structure buffer.

```cs
DateTime GetDate(int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the date format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the date separator used.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | A DateTime value where the Date part is the value retrieved from the Data Structure Buffer.

### Byte\[\] GetHex([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a byte array from the Data Structure buffer, at the given start position for the given length.

```cs
Byte[] GetHex(int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length of the array.

#### Returns

| Type | Description
| --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | A byte array with the buffer contents at the specified start position and for the given length.

### char GetIndicator([int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a character from the specified position in the Data Structure buffer and returns either '0', if the character is '0', or '1'if the character is anything else.

```cs
char GetIndicator(int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | '0' if the character at the given position in the buffer is '0', or '1' otherwise.

### int GetInteger([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets an integer (Int32) value starting at the specified position in the Data Structure buffer.

```cs
int GetInteger(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The integer number starting at the given position in the buffer.

### long GetLong([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets an long (Int64) value starting at the specified position in the Data Structure buffer.

```cs
long GetLong(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | The long number starting at the given position in the buffer.

### Nullable\<decimal\> GetNullableBinary([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a decimal number stored as a Binary decimal number starting at the specified position in the Data Structure buffer.

```cs
Nullable<decimal> GetNullableBinary(int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Binary decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Binary decimal number.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The decimal number value of the Binary decimal number.

### Nullable\<byte\> GetNullableByte([int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a byte value from the specified position in the Data Structure buffer.

```cs
Nullable<byte> GetNullableByte(int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The character at the given position in the buffer.

### Nullable\<char\> GetNullableChar([int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a character from the specified position in the Data Structure buffer.

```cs
Nullable<char> GetNullableChar(int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The character at the given position in the buffer.

### Nullable\<DateTime\> GetNullableDate([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Gets a Date value stored with the specified format and date separator at the specified starting position in the Data Structure buffer.

```cs
Nullable<DateTime> GetNullableDate(int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the date format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the date separator used.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | A DateTime value where the Date part is the value retrieved from the Data Structure Buffer.

### Nullable\<char\> GetNullableIndicator([int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a character from the specified position in the Data Structure buffer and returns either '0', if the character is '0', or '1'if the character is anything else.

```cs
Nullable<char> GetNullableIndicator(int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | '0' if the character at the given position in the buffer is '0', or '1' otherwise.

### Nullable\<int\> GetNullableInteger([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets an integer (Int32) value starting at the specified position in the Data Structure buffer.

```cs
Nullable<int> GetNullableInteger(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The integer number starting at the given position in the buffer.

### Nullable\<long\> GetNullableLong([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets an long (Int64) value starting at the specified position in the Data Structure buffer.

```cs
Nullable<long> GetNullableLong(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The long number starting at the given position in the buffer.

### Nullable\<decimal\> GetNullablePacked([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a decimal number stored as a Packed decimal number starting at the specified position in the Data Structure buffer.

```cs
Nullable<decimal> GetNullablePacked(int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Packed decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Packed decimal number.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The decimal number value of the Packed decimal number.

### Nullable\<short\> GetNullableShort([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a short (Int16) value starting at the specified position in the Data Structure buffer.

```cs
Nullable<short> GetNullableShort(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The short number starting at the given position in the buffer.

### string GetNullableString([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a segment of the Data Structure buffer as a string.

```cs
string GetNullableString(int start, int len)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | 0-based starting position of the string in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | Length of the string to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string of the given length that starts at the given position.

### Nullable\<DateTime\> GetNullableTime([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Gets a Time value stored with the specified format and time separator at the specified starting position in the Data Structure buffer.

```cs
Nullable<DateTime> GetNullableTime(int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the time format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the time separator used.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | A DateTime value where the Time part is the value retrieved from the Data Structure Buffer.

### Nullable\<DateTime\> GetNullableTimestamp([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Gets a Timestamp value stored with the specified timestamp separator at the specified starting position in the Data Structure buffer.

```cs
Nullable<DateTime> GetNullableTimestamp(int start, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the timestamp separator used. Only None or Default are allowed.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | A DateTime value containing the Timestamp value retrieved from the Data Structure Buffer.

### Nullable\<decimal\> GetNullableZoned([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a decimal number stored as a Zoned decimal number starting at the specified position in the Data Structure buffer.

```cs
Nullable<decimal> GetNullableZoned(int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Zoned decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Zoned decimal number.

#### Returns

| Type | Description
| --- | ---
| [Nullable`1](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | The decimal number value of the Zoned decimal number.

### decimal GetPacked([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a decimal number stored as a Packed decimal number starting at the specified position in the Data Structure buffer.

```cs
decimal GetPacked(int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Packed decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Packed decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number value of the Packed decimal number.

### short GetShort([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a short (Int16) value starting at the specified position in the Data Structure buffer.

```cs
short GetShort(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

#### Returns

| Type | Description
| --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | The short number starting at the given position in the buffer.

### string GetString([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a segment of the Data Structure buffer as a string.

```cs
string GetString(int start, int len)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | 0-based starting position of the string in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | Length of the string to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string of the given length that starts at the given position.

### DateTime GetTime([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Gets a Time value stored with the specified format and time separator at the specified starting position in the Data Structure buffer.

```cs
DateTime GetTime(int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the time format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the time separator used.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | A DateTime value where the Time part is the value retrieved from the Data Structure Buffer.

### DateTime GetTimestamp([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Gets a Timestamp value stored with the specified timestamp separator at the specified starting position in the Data Structure buffer.

```cs
DateTime GetTimestamp(int start, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the timestamp separator used. Only None or Default are allowed.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | A DateTime value containing the Timestamp value retrieved from the Data Structure Buffer.

### U GetValue\<U\>([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the value of the field at the requested starting position in the buffer.

```cs
U GetValue<U>(int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Position in the buffer where the field starts.

#### Returns

| Type | Description
| --- | ---
| [U](https://learn.microsoft.com/en-us/dotnet/standard/generics) | The value of the field that starts at the requested buffer position.

### decimal GetZoned([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a decimal number stored as a Zoned decimal number starting at the specified position in the Data Structure buffer.

```cs
decimal GetZoned(int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Zoned decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Zoned decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number value of the Zoned decimal number.

### void Load([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the Data Structure buffer to the given string value, padding with blanks if necessary.

```cs
void Load(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to load into the buffer.

### void ObjectToParm([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dim](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

IDS.ObjectToParm implementation. Converts the Data Structure field values into parameters for calling the given IBMi program.

```cs
void ObjectToParm(As400Program program, Int32[] indices, int dim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter.

### string op_Explicit([DataStructure dataStructure](/reference/runtime/qsys-runtime/data-structure.html))

Casting operator to string. Returns the data structure as a string.

```cs
string op_Explicit(DataStructure dataStructure)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | dataStructure | Data structure to cast to string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### DSDataArea op_Implicit([DataStructure ds](/reference/runtime/qsys-runtime/data-structure.html))

Casting operator to DSDataArea.

```cs
DSDataArea op_Implicit(DataStructure ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ds | The DataStructure object to cast.

#### Returns

| Type | Description
| --- | ---
| [DSDataArea](/reference/runtime/qsys-runtime/ds-data-area.html) | 

### void ParmToObject([As400Program program](/reference/datagate/datagate-client/as400-program.html), [Int32\[\] indices](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [int dim](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

IDS.ParmToObject implementation. Gets the Data Structure field values returned from a call to an IBMi program.

```cs
void ParmToObject(As400Program program, Int32[] indices, int dim)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | program | As400Program object describing the program call.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indices | Array that hold the indices for the current parameter.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | dim | The dimension nesting of the parameter.

### void SetBinary([decimal value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a decimal number as a Binary decimal number starting at the specified position in the Data Structure buffer.

```cs
void SetBinary(decimal value, int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The decimal value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Binary decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Binary decimal number.

### void SetByte([byte value](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a byte value in the specified position in the Data Structure buffer.

```cs
void SetByte(byte value, int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | value | The byte to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

### void SetChar([char val](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a character value in the specified position in the Data Structure buffer.

```cs
void SetChar(char val, int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | val | The character to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

### void SetDate([DateTime value](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Stores the Date part of a DateTime value with the specified format and date separator in the Data Structure buffer.

```cs
void SetDate(DateTime value, int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | value | The DateTime value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the date format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the date separator used.

### void SetHex([Byte\[\] value](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a byte array in the Data Structure buffer, at the given start position for the given length.

```cs
void SetHex(Byte[] value, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | value | The byte array to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length of the array.

### void SetIndicator([char val](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores an indicator value specified as a character in the specified position in the Data Structure buffer.

```cs
void SetIndicator(char val, int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | val | The indicator value as a character.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

### void SetInteger([int value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores an integer (Int32) value starting at the specified position in the Data Structure buffer.

```cs
void SetInteger(int value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | value | The integer number to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

### void SetLong([long value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores an long (Int64) value starting at the specified position in the Data Structure buffer.

```cs
void SetLong(long value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | value | The long number to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

### void SetNullableBinary([Nullable\<decimal\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a decimal number as a Binary decimal number starting at the specified position in the Data Structure buffer.

```cs
void SetNullableBinary(Nullable<decimal> value, int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Decimal\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The decimal value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Binary decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Binary decimal number.

### void SetNullableByte([Nullable\<byte\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a byte value in the specified position in the Data Structure buffer.

```cs
void SetNullableByte(Nullable<byte> value, int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Byte\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The byte to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

### void SetNullableChar([Nullable\<char\> val](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a character value in the specified position in the Data Structure buffer.

```cs
void SetNullableChar(Nullable<char> val, int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | val | The character to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

### void SetNullableDate([Nullable\<DateTime\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Stores the Date part of a DateTime value with the specified format and date separator in the Data Structure buffer.

```cs
void SetNullableDate(Nullable<DateTime> value, int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<DateTime\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The DateTime value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the date format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the date separator used.

### void SetNullableIndicator([Nullable\<char\> val](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int position](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores an indicator value specified as a character in the specified position in the Data Structure buffer.

```cs
void SetNullableIndicator(Nullable<char> val, int position)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Char\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | val | The indicator value as a character.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | position | Position in the Data Structure buffer.

### void SetNullableInteger([Nullable\<int\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores an integer (Int32) value starting at the specified position in the Data Structure buffer.

```cs
void SetNullableInteger(Nullable<int> value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Int32\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The integer number to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

### void SetNullableLong([Nullable\<long\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores an long (Int64) value starting at the specified position in the Data Structure buffer.

```cs
void SetNullableLong(Nullable<long> value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Int64\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The long number to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

### void SetNullablePacked([Nullable\<decimal\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a decimal number as a Packed decimal number starting at the specified position in the Data Structure buffer.

```cs
void SetNullablePacked(Nullable<decimal> value, int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Decimal\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The decimal value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Packed decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Packed decimal number.

### void SetNullableShort([Nullable\<short\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a short (Int16) value starting at the specified position in the Data Structure buffer.

```cs
void SetNullableShort(Nullable<short> value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Int16\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The short number to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

### void SetNullableString([string val](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [char padChar](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a string into a segment the Data Structure buffer, left adjusted. Pads on the right if necessary.

```cs
void SetNullableString(string val, int start, int len, char padChar, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | val | String value to save.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position of the string in the buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | Length of the string.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | padChar | Character to pad the string if necessary. Default is blanks.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | Indicates whether to pad or not. Default is true.

### void SetNullableStringR([string val](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [char padChar](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a string into a segment the Data Structure buffer, right adjusted. Pads on the left if necessary.

```cs
void SetNullableStringR(string val, int start, int len, char padChar, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | val | String value to save.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position of the string in the buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | Length of the string.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | padChar | Character to pad the string if necessary. Default is blanks.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | Indicates whether to pad or not. Default is true.

### void SetNullableTime([Nullable\<DateTime\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Stores the Time part of a DateTime value with the specified format and time separator in the Data Structure buffer.

```cs
void SetNullableTime(Nullable<DateTime> value, int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<DateTime\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The DateTime value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the time format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the time separator used.

### void SetNullableTimestamp([Nullable\<DateTime\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Stores the DateTime value as a Timestamp with the specified timestamp separator in the Data Structure buffer.

```cs
void SetNullableTimestamp(Nullable<DateTime> value, int start, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<DateTime\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The DateTime value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the timestamp separator used. Only None or Default are allowed.

### void SetNullableZoned([Nullable\<decimal\> value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a decimal number as a Zoned decimal number starting at the specified position in the Data Structure buffer.

```cs
void SetNullableZoned(Nullable<decimal> value, int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Nullable\<Decimal\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | value | The decimal value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Zoned decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Zoned decimal number.

### void SetPacked([decimal value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a decimal number as a Packed decimal number starting at the specified position in the Data Structure buffer.

```cs
void SetPacked(decimal value, int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The decimal value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Packed decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Packed decimal number.

### void SetShort([short value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a short (Int16) value starting at the specified position in the Data Structure buffer.

```cs
void SetShort(short value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | value | The short number to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.

### void SetString([string val](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [char padChar](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a string into a segment the Data Structure buffer, left adjusted. Pads on the right if necessary.

```cs
void SetString(string val, int start, int len, char padChar, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | val | String value to save.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position of the string in the buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | Length of the string.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | padChar | Character to pad the string if necessary. Default is blanks.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | Indicates whether to pad or not. Default is true.

### void SetStringR([string val](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [char padChar](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a string into a segment the Data Structure buffer, right adjusted. Pads on the left if necessary.

```cs
void SetStringR(string val, int start, int len, char padChar, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | val | String value to save.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position of the string in the buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | Length of the string.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | padChar | Character to pad the string if necessary. Default is blanks.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | Indicates whether to pad or not. Default is true.

### void SetTime([DateTime value](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeFormat format](/reference/datagate/datagate-common/date-time-format.html), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Stores the Time part of a DateTime value with the specified format and time separator in the Data Structure buffer.

```cs
void SetTime(DateTime value, int start, DateTimeFormat format, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | value | The DateTime value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | format | The DateTimeFormat value that represents the time format to use.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the time separator used.

### void SetTimestamp([DateTime value](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DateTimeSeparator separator](/reference/runtime/qsys-runtime/date-time-separator.html))

Stores the DateTime value as a Timestamp with the specified timestamp separator in the Data Structure buffer.

```cs
void SetTimestamp(DateTime value, int start, DateTimeSeparator separator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | value | The DateTime value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | separator | The DateTimeSeparator value that represents the timestamp separator used. Only None or Default are allowed.

### void SetValue\<U\>([U value](https://learn.microsoft.com/en-us/dotnet/standard/generics), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Sets the value of the field at the requested starting position in the buffer.

```cs
void SetValue<U>(U value, int start)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [U](https://learn.microsoft.com/en-us/dotnet/standard/generics) | value | The value to set.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Position in the buffer where the field starts.

### void SetZoned([decimal value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Stores a decimal number as a Zoned decimal number starting at the specified position in the Data Structure buffer.

```cs
void SetZoned(decimal value, int start, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The decimal value to store.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | Starting position in the Data Structure buffer.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits in the Zoned decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the Zoned decimal number.

### string ToString()

Gets the contents of the data structure as a string.

```cs
string ToString()
```
