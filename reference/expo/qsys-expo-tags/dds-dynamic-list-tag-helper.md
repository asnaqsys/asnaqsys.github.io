---
title: "DdsDynamicListTagHelper class | QSYS API Reference Guide"
description: "Defines a dynamic list selector that retrieves options by invoking a host program."
---

Defines a dynamic list selector that retrieves options by invoking a host program.


**Namespace:** ASNA.QSys.Expo.Tags<br/>
**Assembly:** ASNA.QSys.Expo.Tags.dll


**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

The DdsDynamicListTagHelper renders an input element configured with encoded runtime metadata so the browser can open a dynamic options list.

At render time, it:

1. Collects the target field and parameter element IDs.
2. Registers host-call specifications (library, program, static parameter data, and output length constraints).
3. Emits a data attribute payload used by client logic to request and display options.
4. Optionally applies grid placement style when a column position is provided.

The helper is designed for scenarios where list values depend on host-side logic and current page state.

## Properties

| Type | Name | Description |
| --- | --- | --- |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Col | Gets or sets a value that indicates the horizontal position within a row. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MaxOutputLength | Gets or sets the maximum VARYING length of a character field returned by the host program. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | OptionsPageSize | Gets or sets the number of options visible at a time in the selector. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | LibraryName | Gets or sets the program library or assembly name. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParmsData | Gets or sets comma-separated literal parameter values passed to the host program. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParmsElements | Gets or sets comma-separated HTML element names whose current browser values are passed as host parameters. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ProgramName | Gets or sets the program or class name to be invoked. |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | TargetField | Gets or sets the name of the field that receives the selected value. |

