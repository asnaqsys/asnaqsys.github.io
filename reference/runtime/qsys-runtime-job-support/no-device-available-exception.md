---
title: NoDeviceAvailableException class
---

The exception that is thrown when an operation is attempted when the job is not attached to a device.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [NoDeviceAvailableException](#nodeviceavailableexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the NoDeviceAvailable exception class.

### NoDeviceAvailableException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the NoDeviceAvailable exception class.

```cs
NoDeviceAvailableException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | op | The operation attempted with no device attached to the job.