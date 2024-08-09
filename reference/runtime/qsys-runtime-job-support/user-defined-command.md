---
title: "UserDefinedCommand class      | QSYS API Reference Guide"
description: "Defines the core behavior of user defined commands and provide a base for derived classes. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the core behavior of user defined commands and provide a base for derived classes.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [UserDefinedCommand](#userdefinedcommandicaller)([ICaller](/reference/runtime/qsys-runtime/i-caller.html)) | Called from constructors in derived classes to initialize the command class.

### UserDefinedCommand([ICaller](/reference/runtime/qsys-runtime/i-caller.html))

Called from constructors in derived classes to initialize the command class.

```cs
UserDefinedCommand(ICaller)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | caller | The caller of the command. The caller is typically a program.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ActivationGroup](/reference/runtime/qsys-runtime-job-support/activation-group.html) | ActivationGroup | Gets the command's activation group. |
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | caller | Holds the caller of the command. |
