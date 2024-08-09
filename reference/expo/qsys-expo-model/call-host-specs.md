---
title: "CallHostSpecs class           | QSYS API Reference Guide"
description: "Defines CallHostSpecs class "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines CallHostSpecs class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CallHostSpecs](#callhostspecsstring-string-string-int32-string-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes new instance of CallHostSpecs class given the parameter initializers

### CallHostSpecs([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes new instance of CallHostSpecs class given the parameter initializers

```cs
CallHostSpecs(String, String, String, Int32, String, String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | agentContainer | agent container
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | agentName | agent name
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parmsConstants | parameter constants
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | parmsControlsCount | parameters control's count
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | format name
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parmsFormatFields | parameter format fields
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxOutputLength | maximum output length

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormatName | Gets the format name |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LibraryName | Gets the Library Name |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MaxOutputLength | Gets the Maximum output length |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ParmsConstants | Gets the parameter constants |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ParmsControlsCount | Gets the parameter control's count |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ParmsFormatFields | Gets the parameters format fields |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProgramName | Gets the Program Name |
