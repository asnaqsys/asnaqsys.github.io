---
title: "ASNA.QSys.Runtime Structs"
description: TOC Landing page for ASNA.QSys.Runtime Structs
---

## Remarks

The `ASNA.QSys.Runtime` assembly contains a collection of structs that are used throughout the ASNA QSys system. These structs are value types that encapsulate small groups of related variables, such as the parameters of a method or the elements of a data structure.

These structs cover a wide range of functionalities, from defining fixed-size arrays of various data types, to holding fixed-date, fixed-time, and fixed-timestamp values in specified formats, to representing IBM i RPG Indicators.

Here are some key points to remember when working with these structs:

- **Efficiency**: Structs are value types and are typically more efficient than classes when they encapsulate small amounts of data.
- **Immutability**: Structs are immutable by default, which can make your code safer and easier to reason about.
- **Data Structures**: Many of these structs are used to define data structures, making it easier to work with complex data in a structured way.

Remember to refer to the individual struct documentation for specific details about each struct's fields, properties, methods, and usage.

| Type | Description |
| --- | --- |
| [CharArray\<T\>](/reference/runtime/qsys-runtime/char-array-1.html) | Represents a unidimensional fixed-size array of characters. |
| [CharArrayInDS\<T\>](/reference/runtime/qsys-runtime/char-array-in-ds-1.html) | Describes a fixed size array of characters contained in a DataStructure. |
| [FixedArray\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-array-2.html) | Defines the functionality of a fixed-sized unidimensional array. |
| [FixedDate\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-date-2.html) | Holds a fixed-date value in the specified format and with the given separator. |
| [FixedDateArray\<T1, T2, T3\>](/reference/runtime/qsys-runtime/fixed-date-array-3.html) | Defines the functionality of a fixed-sized unidimensional array of FixedDate elements. |
| [FixedDateArrayInDS\<T1, T2, T3\>](/reference/runtime/qsys-runtime/fixed-date-array-in-ds-3.html) | Describes a fixed size array of FixedDate contained in a DataStructure. |
| [FixedDecimal\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-decimal-2.html) | Holds a fixed-decimal value with the specified number of digits and decimal positions. |
| [FixedDecimalArray\<T1, T2, T3\>](/reference/runtime/qsys-runtime/fixed-decimal-array-3.html) | Defines the functionality of a fixed-sized unidimensional array of FixedDecimal elements. |
| [FixedDecimalArrayInDS\<T1, T2, T3\>](/reference/runtime/qsys-runtime/fixed-decimal-array-in-ds-3.html) | Describes a fixed size array of FixedDecimal contained in a DataStructure. |
| [FixedString\<T\>](/reference/runtime/qsys-runtime/fixed-string-1.html) | Holds a fixed-string value with the specified length. |
| [FixedStringArray\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-string-array-2.html) | Defines the functionality of a fixed-sized unidimensional array of FixedString elements. |
| [FixedStringArrayInDS\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-string-array-in-ds-2.html) | Describes a fixed size array of FixedString contained in a DataStructure. |
| [FixedTime\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-time-2.html) | Holds a fixed-time value in the specified format and with the given separator. |
| [FixedTimeArray\<T1, T2, T3\>](/reference/runtime/qsys-runtime/fixed-time-array-3.html) | Defines the functionality of a fixed-sized unidimensional array of FixedTime elements. |
| [FixedTimeArrayInDS\<T1, T2, T3\>](/reference/runtime/qsys-runtime/fixed-time-array-in-ds-3.html) | Describes a fixed size array of FixedTime contained in a DataStructure. |
| [FixedTimestamp\<T\>](/reference/runtime/qsys-runtime/fixed-timestamp-1.html) | Holds a fixed-timestamp value with the given separator. |
| [FixedTimestampArray\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-timestamp-array-2.html) | Defines the functionality of a fixed-sized unidimensional array of FixedTimestamp elements. |
| [FixedTimestampArrayInDS\<T1, T2\>](/reference/runtime/qsys-runtime/fixed-timestamp-array-in-ds-2.html) | Describes a fixed size array of FixedTimestamp contained in a DataStructure. |
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | This class represents an IBM i RPG Indicator.  |
| [IndicatorArray\<T\>](/reference/runtime/qsys-runtime/indicator-array-1.html) | Defines the functionality of a fixed-sized unidimensional array of Indicator elements. |
| [IndicatorArrayInDS\<T\>](/reference/runtime/qsys-runtime/indicator-array-in-ds-1.html) | Describes a fixed size array of Indicators contained in a DataStructure. |
| [IntArrayInDS\<T\>](/reference/runtime/qsys-runtime/int-array-in-ds-1.html) | Describes a fixed size array of integers contained in a DataStructure. |
| [Layout](/reference/runtime/qsys-runtime/layout.html) | Defines a layout for a field in a data structure. |
| [LongArrayInDS\<T\>](/reference/runtime/qsys-runtime/long-array-in-ds-1.html) | Describes a fixed size array of long numbers contained in a DataStructure. |
| [ShortArrayInDS\<T\>](/reference/runtime/qsys-runtime/short-array-in-ds-1.html) | Describes a fixed size array of short numbers contained in a DataStructure. |
