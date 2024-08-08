---
title: "DataGateException class       | QSYS API Reference Guide"
description: "DataGate operation on file -filename- caused -datagate exception- exception. "
last_modified_at: 2024-08-08T21:41:46Z
---

DataGate operation on file -filename- caused -datagate exception- exception.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DataGateException](#datagateexceptionstring-dgexception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [dgException](/reference/datagate/datagate-common/dg-exception.html)) | Constructor that takes the -filename- and the Datagate -exception instance- that caused the Exception.

### DataGateException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [dgException](/reference/datagate/datagate-common/dg-exception.html))

Constructor that takes the -filename- and the Datagate -exception instance- that caused the Exception.

```cs
DataGateException(String, dgException)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Filename.
| [dgException](/reference/datagate/datagate-common/dg-exception.html) | e | Datagate exception.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DclFileName | Gets the name of the declared filename that caused the exception. |

## Methods

| Signature | Description |
| --- | --- |
| [ToString()](#string-tostring) | Formats exception using DataGate exception error formatting.

### string ToString()

Formats exception using DataGate exception error formatting.

```cs
string ToString()
```
