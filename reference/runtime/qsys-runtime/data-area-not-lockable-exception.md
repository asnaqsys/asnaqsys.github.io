---
title: "DataAreaNotLockableException class | QSYS API Reference Guide"
description: "DataArea Exception issued when a DataArea fails to Unlock. "
last_modified_at: 2024-07-09T17:00:49Z
---

DataArea Exception issued when a DataArea fails to Unlock.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DataAreaNotLockableException](#dataareanotlockableexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Creates a DataAreaNotLockableException object, with an inner exception. Sets the message to: Data area -data-area-name- could not be locked.

### DataAreaNotLockableException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Creates a DataAreaNotLockableException object, with an inner exception. Sets the message to: Data area -data-area-name- could not be locked.

```cs
DataAreaNotLockableException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | Inner exception.
