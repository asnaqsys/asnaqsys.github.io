---
title: "Program class                 | QSYS API Reference Guide"
description: "Defines the core behavior of a program and provides a base for migrated derived classes. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the core behavior of a program and provides a base for migrated derived classes.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Module](/reference/runtime/qsys-runtime-job-support/module.html) --> [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [BeginCall\<T\>](#t-begincall-t-icaller-caller)([ICaller](/reference/runtime/qsys-runtime/i-caller.html)) | Prepares a program for execution by getting an instance of the program and pushing it in the invocation stack.
| [EndCall()](#indicator-endcall) | Marks the end of a program execution by popping it from the invocation stack and potentially deactivating it when the program's LR indicator is on.

### T BeginCall\<T\>([ICaller caller](/reference/runtime/qsys-runtime/i-caller.html))

Prepares a program for execution by getting an instance of the program and pushing it in the invocation stack.

```cs
T BeginCall<T>(ICaller caller)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | caller | The Program or Job preparing the program.

#### Returns

| Type | Description
| --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | The prepared program instance.

### Indicator EndCall()

Marks the end of a program execution by popping it from the invocation stack and potentially deactivating it when the program's LR indicator is on.

```cs
Indicator EndCall()
```
