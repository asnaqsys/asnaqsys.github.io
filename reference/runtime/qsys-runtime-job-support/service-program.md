---
title: "ServiceProgram class          | QSYS API Reference Guide"
description: "Defines the core behavior of a service program and provides a base for migrated derived classes. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the core behavior of a service program and provides a base for migrated derived classes.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Module](/reference/runtime/qsys-runtime-job-support/module.html) --> [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ServiceProgram](#serviceprogramcommonprogram)([CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html)) | Called from constructors in derived classes to initialize the service program class. 

### ServiceProgram([CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html))

Called from constructors in derived classes to initialize the service program class. 

```cs
ServiceProgram(CommonProgram)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html) | containerProgram | If the service program is used a module, this parameter is a reference to the program using it. Defaults to null.

## Methods

| Signature | Description |
| --- | --- |
| [GetInstance\<T\>](#t-getinstance-t-icaller-caller)([ICaller](/reference/runtime/qsys-runtime/i-caller.html)) | Gets an instance of a service program. The instance can be an existing one if it is found in the Job otherwise a new one is created. 

### T GetInstance\<T\>([ICaller caller](/reference/runtime/qsys-runtime/i-caller.html))

Gets an instance of a service program. The instance can be an existing one if it is found in the Job otherwise a new one is created. 

```cs
T GetInstance<T>(ICaller caller)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | caller | The job or program seeking the service program instance.

#### Returns

| Type | Description
| --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | The desired service program object.
