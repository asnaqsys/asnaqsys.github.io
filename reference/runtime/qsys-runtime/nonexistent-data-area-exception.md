---
title: "NonexistentDataAreaException class"
description: "DataArea Exception issued when requesting a non-existing DataArea. "
last_modified_at: 2024-08-09T16:18:25Z
---

DataArea Exception issued when requesting a non-existing DataArea.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [NonexistentDataAreaException](#nonexistentdataareaexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates an NonexistentDataAreaException object. Sets the message to: Data area 'data-area-name' does not exist.
| [NonexistentDataAreaException](#nonexistentdataareaexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Creates an NonexistentDataAreaException object, with an inner exception. Sets the message to: Data area 'data-area-name' does not exist.

### NonexistentDataAreaException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Creates an NonexistentDataAreaException object. Sets the message to: Data area 'data-area-name' does not exist.

```cs
NonexistentDataAreaException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.

### NonexistentDataAreaException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Creates an NonexistentDataAreaException object, with an inner exception. Sets the message to: Data area 'data-area-name' does not exist.

```cs
NonexistentDataAreaException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | Inner exception.
