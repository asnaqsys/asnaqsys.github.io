---
title: "ActivationGroup class         | QSYS API Reference Guide"
description: "Provides the facilities to organize the instances of programs and service programs into related groups. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides the facilities to organize the instances of programs and service programs into related groups.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Count | Gets the number of programs active in the activation group. |
| [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html) | DynamicCreator | Gets the program that cause the *NEW dynamic creation of the activation group. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsDynamic | Gets a value that indicates whether the activation group was created *NEW for a program and will be dynamically deleted when the program ends. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Gets the name of the activation group. |

## Methods

| Signature | Description |
| --- | --- |
| [EndPrograms()](#void-endprograms) | Disposes of all the programs belonging to the activation group.

### void EndPrograms()

Disposes of all the programs belonging to the activation group.

```cs
void EndPrograms()
```
