---
title: "FieldType class"
description: "Represents the type of a field in a data structure. "
last_modified_at: 2024-08-09T17:25:07Z
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
| [GetSystemTypeOfType](field-type-getsystemtypeoftype.html#type-getsystemtypeoftype-datatypes-dt-int-bytelength)([DataTypes](/reference/datagate/datagate-common/data-types.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the corresponding .NET type for a given DataTypes value and byte length.
| [NewBinary](field-type-newbinary.html#fieldtype-newbinary-int-prec-int-scale)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a binary field.
| [NewByte()](field-type-newbyte.html#fieldtype-newbyte) | Creates a new FieldType instance representing a byte field.
| [NewChar](field-type-newchar.html#fieldtype-newchar-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a character field.
| [NewDate](field-type-newdate.html#fieldtype-newdate-datetimeformat-fmt)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates a new FieldType instance representing a date field.
| [NewDBCS](field-type-newdbcs.html#fieldtype-newdbcs-int-length-dbcsformat-fmt)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DbcsFormat](/reference/datagate/datagate-common/dbcs-format.html)) | Creates a new FieldType instance representing a DBCS field.
| [NewDontCare](field-type-newdontcare.html#fieldtype-newdontcare-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a DontCare field.
| [NewFloat](field-type-newfloat.html#fieldtype-newfloat-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a floating point field.
| [NewHex](field-type-newhex.html#fieldtype-newhex-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a hexadecimal field.
| [NewInteger](field-type-newinteger.html#fieldtype-newinteger-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing an integer field.
| [NewPacked](field-type-newpacked.html#fieldtype-newpacked-int-prec-int-scale)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a packed decimal field.
| [NewTime](field-type-newtime.html#fieldtype-newtime-datetimeformat-fmt)([DateTimeFormat](/reference/datagate/datagate-common/date-time-format.html)) | Creates a new FieldType instance representing a time field.
| [NewTimestamp()](field-type-newtimestamp.html#fieldtype-newtimestamp) | Creates a new FieldType instance representing a timestamp field.
| [NewUnicode](field-type-newunicode.html#fieldtype-newunicode-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a Unicode field.
| [NewZoned](field-type-newzoned.html#fieldtype-newzoned-int-prec-int-scale)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new FieldType instance representing a zoned decimal field.

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

