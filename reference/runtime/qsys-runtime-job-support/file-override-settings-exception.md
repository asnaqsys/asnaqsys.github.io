---
title: "FileOverrideSettingsException class"
description: "The exception that is thrown when a file override specified in the config file is invalid. "
last_modified_at: 2024-08-09T16:18:25Z
---

The exception that is thrown when a file override specified in the config file is invalid.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [FileOverrideSettingsException](#fileoverridesettingsexceptionstring-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileOverrideSettings exception class.

### FileOverrideSettingsException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the FileOverrideSettings exception class.

```cs
FileOverrideSettingsException(String, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The file stated in the invalid specification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | optionName | The override option name stated in the invalid specification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | optionValue | The override option value stated in the invalid specification.
