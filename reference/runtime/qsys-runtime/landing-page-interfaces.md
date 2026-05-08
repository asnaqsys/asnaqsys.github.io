---
title: "ASNA.QSys.Runtime Interfaces"
description: TOC Landing page for ASNA.QSys.Runtime Interfaces
---

## Remarks

The `ASNA.QSys.Runtime` assembly contains a collection of interfaces that are used throughout the ASNA QSys system. These interfaces define a contract of operations, properties, and events that classes can implement, providing a way to achieve polymorphism and increase the flexibility and interoperability of the system.

These interfaces cover a wide range of functionalities, from defining date/time formats and separators, to identifying classes that participate in the ActivationGroup logic, to defining functionality for files that participate in the RPG cycle.

Here are some key points to remember when working with these interfaces:

- **Polymorphism**: By defining a common interface, different classes can implement the same interface in different ways. This allows you to write code that can work with objects of any class that implements a particular interface.
- **Flexibility**: Interfaces allow you to create systems that are flexible and easily extensible. You can add new classes that implement these interfaces without having to change the existing code that uses the interfaces.
- **Interoperability**: These interfaces provide a consistent way to interact with different parts of the ASNA QSys system, increasing the interoperability of your code.

Remember to refer to the individual interface documentation for specific details about each interface's contract and usage.


| Type | Description |
| --- | --- |
| [_Blank](/reference/runtime/qsys-runtime/-blank.html) | Describes the Blank as date/time separator in the declaration of date/time types. |
| [_Colon](/reference/runtime/qsys-runtime/-colon.html) | Describes the Colon (:) as date/time separator in the declaration of date/time types. |
| [_Comma](/reference/runtime/qsys-runtime/-comma.html) | Describes the Comma (,) as date/time separator in the declaration of date/time types. |
| [_Default](/reference/runtime/qsys-runtime/-default.html) | Describes the Default date/time separator in the declaration of date/time types. |
| [_DMY](/reference/runtime/qsys-runtime/dmy.html) | Describes the DMY date/time format in the declaration of date/time types. |
| [_Dot](/reference/runtime/qsys-runtime/-dot.html) | Describes the Dot (.) as date/time separator in the declaration of date/time types. |
| [_EUR](/reference/runtime/qsys-runtime/eur.html) | Describes the EUR date/time format in the declaration of date/time types. |
| [_HMS](/reference/runtime/qsys-runtime/hms.html) | Describes the HMS date/time format in the declaration of date/time types. |
| [_ISO](/reference/runtime/qsys-runtime/iso.html) | Describes the ISO date/time format in the declaration of date/time types. |
| [_JIS](/reference/runtime/qsys-runtime/jis.html) | Describes the JIS date/time format in the declaration of date/time types. |
| [_JUL](/reference/runtime/qsys-runtime/jul.html) | Describes the JUL date/time format in the declaration of date/time types. |
| [_MDY](/reference/runtime/qsys-runtime/mdy.html) | Describes the MDY date/time format in the declaration of date/time types. |
| [_Minus](/reference/runtime/qsys-runtime/-minus.html) | Describes the Minus sign (-) as date/time separator in the declaration of date/time types. |
| [_None](/reference/runtime/qsys-runtime/-none.html) | Describes the Slash (/) as date/time separator in the declaration of date/time types. |
| [_Slash](/reference/runtime/qsys-runtime/-slash.html) | Describes the Slash (/) as date/time separator in the declaration of date/time types. |
| [_USA](/reference/runtime/qsys-runtime/usa.html) | Describes the USA date/time format in the declaration of date/time types. |
| [_YMD](/reference/runtime/qsys-runtime/ymd.html) | Describes the YMD date/time format in the declaration of date/time types. |
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | Identifies a class that participates in the ActivationGroup logic. A class that uses CALLD must implement this interface. |
| [ICycleFile](/reference/runtime/qsys-runtime/i-cycle-file.html) | Defines functionality that a file which participates in the RPG cycle must provide. |
| [IDateTimeFormat](/reference/runtime/qsys-runtime/i-date-time-format.html) | Base interface for interfaces used as date/time formats in the declaration of date/time types. |
| [IDateTimeSeparator](/reference/runtime/qsys-runtime/i-date-time-separator.html) | Base interface for interfaces used as date/time separators in the declaration of date/time types. |
| [IDigit](/reference/runtime/qsys-runtime/i-digit.html) | Interface that identifies a subset of length type arguments that represent digits, from 0 to 9. |
| [IDim](/reference/runtime/qsys-runtime/i-dim.html) | Interface that identifies types to be used as dimension type arguments in fixed array declarations. |
| [IDisplayFile](/reference/runtime/qsys-runtime/i-display-file.html) | Defines the interface for display files, providing methods and properties for interacting with display file records and formats. |
| [IDS](/reference/runtime/qsys-runtime/ids.html) | Defines the basic set of operations for a data structure. |
| [IDSArrayField](/reference/runtime/qsys-runtime/ids-array-field.html) | Describes the common operations for an array field in a Data Structure. |
| [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html) | This interface should be implemented by any DataStructure class if an object of its type will be passed as a parameter to a program in the IBMi. |
| [IDSDataArea](/reference/runtime/qsys-runtime/ids-data-area.html) | Describes a data structure that can be stored in a data area. |
| [IDSField](/reference/runtime/qsys-runtime/ids-field.html) | Describes the common operations over a field in a Data Structure. |
| [IFixedArray\<T1, T2\>](/reference/runtime/qsys-runtime/i-fixed-array-2.html) | Describes the minimum functionality of a free-standing fixed sized array. |
| [IFixedArrayBase\<T1, T2\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html) | Base interface for all fixed sized arrays in the fixed-sized type framework. These arrays are unidimensional. |
| [IFixedArrayInDS\<T1, T2\>](/reference/runtime/qsys-runtime/i-fixed-array-in-ds-2.html) | Describes minimum operations for a fixed size array contained in a DataStructure. |
| [IFixedDateTime](/reference/runtime/qsys-runtime/i-fixed-date-time.html) | Declares the basic functionality of a fixed datetime type. |
| [IFixedSizeType](/reference/runtime/qsys-runtime/i-fixed-size-type.html) | Declares the basic functionality of a fixed-size type. |
| [IFixedSizeType\<T\>](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | Declares the basic functionality of a fixed-size generic type. |
| [ILayout](/reference/runtime/qsys-runtime/i-layout.html) | Defines operations for objects describing fields in a data structure. |
| [ILen](/reference/runtime/qsys-runtime/i-len.html) | Interface that identifies types to be used as length type arguments in fixed type declarations. |
| [IMODS](/reference/runtime/qsys-runtime/imods.html) | Describes the set of operations of a multi-occurrence data structure. |
| [INumber](/reference/runtime/qsys-runtime/i-number.html) | Interface that identifies a subset of length type arguments, fron 0 to 29. |
| [IWebDisplayFileProvider](/reference/runtime/qsys-runtime/i-web-display-file-provider.html) | Web Display File Provider Interface. It contains methods to handle all Input and Output operations on the file. |
