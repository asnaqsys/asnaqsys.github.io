---
title: "UnlockedDataAreaException class"
description: "DataArea Exception issued when attempting to unlock a DataArea that is not locked. "
last_modified_at: 2024-08-09T16:18:25Z
---

DataArea Exception issued when attempting to unlock a DataArea that is not locked.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [UnlockedDataAreaException](#unlockeddataareaexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates an UnlockedDataAreaException object. Sets the message to: Data area -data-area-name- is not locked.

### UnlockedDataAreaException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Creates an UnlockedDataAreaException object. Sets the message to: Data area -data-area-name- is not locked.

```cs
UnlockedDataAreaException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
