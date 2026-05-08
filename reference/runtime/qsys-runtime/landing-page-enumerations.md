---
title: "ASNA.QSys.Runtime Enumerations"
description: TOC Landing page for ASNA.QSys.Runtime Enumerations
---

## Remarks

The `ASNA.QSys.Runtime` assembly contains a collection of enumerations that are used throughout the ASNA QSys system. These enumerations provide a set of predefined constants that make the code more readable and less prone to errors.

These enumerations cover a wide range of functionalities, from defining the valid values for date/time fixed types, specifying the type of Cycle routine to call, to describing the flag that records the status of a workstation dataset as it is processed.

Here are some key points to remember when working with these enumerations:

- **Readability**: Using these enumerations makes your code more readable, as they provide meaningful names for a set of related values.
- **Error Prevention**: By using enumerations, you can reduce the likelihood of errors caused by passing in invalid values.
- **Consistency**: These enumerations provide a consistent way to handle sets of related values across your application.

Remember to refer to the individual enumeration documentation for specific details about each enumeration's values and usage.

| Type | Description |
| --- | --- |
| [DateTimeDataKind](/reference/runtime/qsys-runtime/date-time-data-kind.html) | Describes the valid values for Kind in a date/time fixed type. |
| [DateTimeSeparator](/reference/runtime/qsys-runtime/date-time-separator.html) | DateTimeSeparator describes the character separator to use. |
| [DbcsType](/reference/runtime/qsys-runtime/dbcs-type.html) | Defines values that describe the kind of DBCS character string of a DBCS field. |
| [DecimalKind](/reference/runtime/qsys-runtime/decimal-kind.html) | Indicates the kind of decimal field. |
| [DurationCode](/reference/runtime/qsys-runtime/duration-code.html) | Describes the valid durations to use in date/time operations. |
| [EditCodes](/reference/runtime/qsys-runtime/edit-codes.html) | Name of Edit-Codes which define output formatting patterns for business numeric data. |
| [InfSrReturnPoint](/reference/runtime/qsys-runtime/inf-sr-return-point.html) | Defines the possible execution state where the program cycle is at any given time. |
| [LayoutType](/reference/runtime/qsys-runtime/layout-type.html) | Contains enumeration values to identify the type of data in a layout. |
| [Limits](/reference/runtime/qsys-runtime/limits.html) | Defines the maximum limits for decimal values, including the maximum number of digits, integral digits, and decimal positions. |
| [NameStoreOptions](/reference/runtime/qsys-runtime/name-store-options.html) | Defines flags that tell the name store which name sources to use. |
| [OpenAccessDspF](/reference/runtime/qsys-runtime/open-access-dsp-f.html) | Enumerates the various supported files for Open Access RPG. |
| [Routine](/reference/runtime/qsys-runtime/routine.html) | Specifies the type of Cycle routine to call. |
| [SearchType](/reference/runtime/qsys-runtime/search-type.html) | Type of search to perform. |
| [ServerSupport](/reference/runtime/qsys-runtime/server-support.html) | For interactive applications that use a virtual terminal, this enum is used to select whether to start a server on the IBMi side. |
| [TestNumericResult](/reference/runtime/qsys-runtime/test-numeric-result.html) | The possible results of a TestNumeric operation. |
| [VirtualTerminal](/reference/runtime/qsys-runtime/virtual-terminal.html) | Available virtual terminal options for Monarch applications against the IBMi. |
| [vxAdjust](/reference/runtime/qsys-runtime/vx-adjust.html) | Half adjust options. |
| [WrfOptions](/reference/runtime/qsys-runtime/wrf-options.html) | For future expansion, options when obtaining the record format of a display file. |
| [WsDsStatus](/reference/runtime/qsys-runtime/ws-ds-status.html) | Describes the flag that records the status of a workstation dataset as it is processed. |
