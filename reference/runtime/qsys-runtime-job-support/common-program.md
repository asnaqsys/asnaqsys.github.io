---
title: "CommonProgram class           | QSYS API Reference Guide"
description: "Defines the core behavior of programs and service programs. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the core behavior of programs and service programs.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Module](/reference/runtime/qsys-runtime-job-support/module.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CommonProgram()](#commonprogram) | Called from constructors in derived classes to initializes the common program class. 
| [CommonProgram](#commonprogramcommonprogram)([CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html)) | Called from constructors in derived classes to initializes the common program class. 

### CommonProgram()

Called from constructors in derived classes to initializes the common program class. 

```cs
CommonProgram()
```

### CommonProgram([CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html))

Called from constructors in derived classes to initializes the common program class. 

```cs
CommonProgram(CommonProgram)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html) | containerProgram | If the program is used a module, this parameter is a reference to the program using it. Defaults to null.

## Methods

| Signature | Description |
| --- | --- |
| [Dispose](#void-disposebool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Called to release the managed and unmanaged resources used by the current instance of the CommonProgram class.
| [GetModule<T>()](#t-getmodule-t) | Gets a constituent module of this program.
| [GetServiceModule<T>()](#t-getservicemodule-t) | Gets a constituent module of one of the service programs being used by this program.

### void Dispose([bool disposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Called to release the managed and unmanaged resources used by the current instance of the CommonProgram class.

```cs
void Dispose(bool disposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | true to release managed and unmanaged resources; false to release only unmanaged resources.

### T GetModule<T>()

Gets a constituent module of this program.

```cs
T GetModule<T>()
```

### T GetServiceModule<T>()

Gets a constituent module of one of the service programs being used by this program.

```cs
T GetServiceModule<T>()
```
