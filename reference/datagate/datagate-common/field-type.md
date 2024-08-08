---
title: "FieldType class               | QSYS API Reference Guide"
description: "Represents the type of a field in a data structure. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents the type of a field in a data structure.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

## Remarks
The FieldType class provides a way to define the type of a field in a data structure, 
including its data type, length, precision, scale, and format for date/time and DBCS fields.
It also provides methods to create new instances of FieldType for specific data types.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ByteLength | Gets the byte length of the field. |
| [DataTypes](/reference/datagate/datagate-common/data-types.html) | DataType | Gets the data type of the field. |
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | DateTime | Gets the date/time format of the field. This is used for date and time types. |
| [DbcsFormat](/reference/datagate/datagate-common/dbcs-format.html) | Dbcs | Gets the DBCS format of the field. This is used for DBCS types. |
| [PropertyCollection](https://learn.microsoft.com/en-us/dotnet/api/system.data.propertycollection?view=net-8.0) | ExtendedProperties | Gets the collection of extended properties for the field. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Precision | Gets the precision of the field. This is used for decimal types. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Scale | Gets the scale of the field. This is used for decimal types. |

## Methods

| Signature | Description |
| --- | --- |
| [GetSystemTypeOfType](#type-getsystemtypeoftypedatatypes-dt-int-bytelength)([DataTypes](/reference/datagate/datagate-common/data-types.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the corresponding .NET type for a given DataTypes value and byte length.
| [NewBinary](#fieldtype-newbinaryint-prec-int-scale)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a binary field.
| [NewByte()](#fieldtype-newbyte) | Creates a new FieldType instance representing a byte field.
| [NewChar](#fieldtype-newcharint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a character field.
| [NewDate](#fieldtype-newdatedatetimeformat-fmt)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates a new FieldType instance representing a date field.
| [NewDBCS](#fieldtype-newdbcsint-length-dbcsformat-fmt)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DbcsFormat](/reference/datagate/datagate-common/dbcs-format.html)) | Creates a new FieldType instance representing a DBCS field.
| [NewDontCare](#fieldtype-newdontcareint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a DontCare field.
| [NewFloat](#fieldtype-newfloatint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a floating point field.
| [NewHex](#fieldtype-newhexint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a hexadecimal field.
| [NewInteger](#fieldtype-newintegerint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing an integer field.
| [NewPacked](#fieldtype-newpackedint-prec-int-scale)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a packed decimal field.
| [NewTime](#fieldtype-newtimedatetimeformat-fmt)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates a new FieldType instance representing a time field.
| [NewTimestamp()](#fieldtype-newtimestamp) | Creates a new FieldType instance representing a timestamp field.
| [NewUnicode](#fieldtype-newunicodeint-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a Unicode field.
| [NewZoned](#fieldtype-newzonedint-prec-int-scale)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a zoned decimal field.

### Type GetSystemTypeOfType([DataTypes dt](/reference/datagate/datagate-common/data-types.html), [int byteLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the corresponding .NET type for a given DataTypes value and byte length.

```cs
Type GetSystemTypeOfType(DataTypes dt, int byteLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataTypes](/reference/datagate/datagate-common/data-types.html) | dt | The DataTypes value to get the .NET type for.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | byteLength | The byte length of the data type.

#### Returns

| Type | Description
| --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | The corresponding .NET type, or null if no match is found.

### FieldType NewBinary([int prec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int scale](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

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

### FieldType NewByte()

Creates a new FieldType instance representing a byte field.

```cs
FieldType NewByte()
```

### FieldType NewChar([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a character field.

```cs
FieldType NewChar(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the character field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewDate([DateTimeFormat fmt](/reference/datagate/datagate-common/date-time-format.html))

Creates a new FieldType instance representing a date field.

```cs
FieldType NewDate(DateTimeFormat fmt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | fmt | The format of the date field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewDBCS([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DbcsFormat fmt](/reference/datagate/datagate-common/dbcs-format.html))

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

### FieldType NewDontCare([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a DontCare field.

```cs
FieldType NewDontCare(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the DontCare field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewFloat([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a floating point field.

```cs
FieldType NewFloat(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the floating point field. It should be either 4 or 8.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewHex([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a hexadecimal field.

```cs
FieldType NewHex(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the hexadecimal field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewInteger([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

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

### FieldType NewPacked([int prec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int scale](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a packed decimal field.

```cs
FieldType NewPacked(int prec, int scale)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | prec | The total number of digits in the packed decimal field.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | scale | The number of digits to the right of the decimal point in the packed decimal field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewTime([DateTimeFormat fmt](/reference/datagate/datagate-common/date-time-format.html))

Creates a new FieldType instance representing a time field.

```cs
FieldType NewTime(DateTimeFormat fmt)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html) | fmt | The format of the time field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewTimestamp()

Creates a new FieldType instance representing a timestamp field.

```cs
FieldType NewTimestamp()
```

### FieldType NewUnicode([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a Unicode field.

```cs
FieldType NewUnicode(int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the Unicode field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

### FieldType NewZoned([int prec](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int scale](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a new FieldType instance representing a zoned decimal field.

```cs
FieldType NewZoned(int prec, int scale)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | prec | The total number of digits in the zoned decimal field.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | scale | The number of digits to the right of the decimal point in the zoned decimal field.

#### Returns

| Type | Description
| --- | ---
| [FieldType](/reference/datagate/datagate-common/field-type.html) | A new FieldType instance.

## Example 1. Use of NewTimestamp method example.


```cs 
  /* Use the already initialized As400OProgram "timeProg" to set the
   * value of a DateTime variable. This program accepts a timestamp data type
   * whose time format is ISO as its sole parameter, which it does not
   * read but uses to return data. */

  ProgParmType as400Time = new ProgParmType("TimeISO", 0, FieldType.NewTimestamp());
  ProgParm timeParm = new ProgParm(as400Time, DataDirection.Output);
  timeProg.AppendParm(timeParm);

  timeProg.Execute();

  DateTime currentTime;
  currentTime = Convert.ToDateTime(timeProg.ParmToObject(timeParm, Type.GetType("System.DateTime"), 0));
  /* Unlike the IBM i FieldType NewTime or NewDate, NewTimeStamp contains both date and time
   * values. */
```

## Example 2. Use of NewDate method example.

```cs 
  /* Create a parms list to pass to a pre-initialized As400Program object.
   * We want to pass one date with time format *USA and another with time
   * format *ISO. Other time formats are available in the DateTimeFormat
   * enumeration as well. */
  DateTime DateUSA = System.DateTime.Now;
  DateTime DateISO = System.DateTime.Now;

  ProgParmType type1 = new ProgParmType("DateUSA", 0, FieldType.NewDate(DateTimeFormat.USA));
  ProgParmType type2 = new ProgParmType("DateISO", 0, FieldType.NewDate(DateTimeFormat.ISO));
  ProgParm parm1 = new ProgParm(type1, DataDirection.InputOutput);
  ProgParm parm2 = new ProgParm(type2, DataDirection.InputOutput);

  prog.AppendParm(parm1);
  prog.AppendParm(parm2);

  /* In the lines below, we assign the IBM i program parameters
   * values from our .NET variables. */
  prog.ObjectToParm(parm1, DateUSA, 0);
  prog.ObjectToParm(parm1, DateISO, 0);

  /* Call the program. */
  prog.Execute();

  /* The parameters can be bidirectional and thus return data as well. 
   * To use that data, we assign the values of the parameters back to our
   * .NET variables. */
  DateUSA = Convert.ToDateTime(prog.ParmToObject(parm1, DateUSA.GetType(), 0));
  DateISO = Convert.ToDateTime(prog.ParmToObject(parm2, DateUSA.GetType(), 0));
  /* IMPORTANT NOTE: The time and date data types do not return all the information
   * which a .NET DateTime can contain. Specifically, if you specify a parm as a NewTime,
   * the data portion of the returned DateTime will be set to MinValue. The same will
   * happen to the time portion of a variable if its IBM i parm was set to be a NewDate. */
```
