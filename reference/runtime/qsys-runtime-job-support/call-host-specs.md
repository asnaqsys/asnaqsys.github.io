---
title: "CallHostSpecs class           | QSYS API Reference Guide"
description: "Packages the specification of a remote program call command and its parameters. "
last_modified_at: 2024-08-08T21:41:46Z
---

Packages the specification of a remote program call command and its parameters.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CallHostSpecs](#callhostspecsstring-string-string-int32-string-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the CallHostSpecs class.

### CallHostSpecs([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the CallHostSpecs class.

```cs
CallHostSpecs(String, String, String, Int32, String, String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | agentContainer | The library or assembly name containing the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The name of the program to be called.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parmsConstants | The comma separated list of constants to be passed as parameters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | parmsControlsCount | The number of control values to be passed as parameters.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | The name of a record format whose field values are to be passed as parameters.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parmsFormatFields | The comma separated list of fields whose values are to be passed as parameters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxOutputLength | The maximum length expected as a return value from the called program.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormatName | Gets the name of the record format to use to find the parameters. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LibraryName | Gets the IBM i Library Name or .NET Assembly name where program resides. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MaxOutputLength | Gets the Maximum length of result from program call. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ParmsConstants | Gets the comma separated list of constant parameters to be passed to the program. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ParmsControlsCount | Gets the number of controls used as parameters to be passed to the program. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ParmsFormatFields | Gets the comma separated list of field names whose values in a record format, are used as parameters to be passed to the program. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProgramName | Gets the Program Name to call. |
