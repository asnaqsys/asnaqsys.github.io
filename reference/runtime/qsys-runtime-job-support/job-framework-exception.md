---
title: "JobFrameworkException class   | QSYS API Reference Guide"
description: "Defined the core behavior of exceptions thrown by Monarch Base and provides a base for derived exceptions. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defined the core behavior of exceptions thrown by Monarch Base and provides a base for derived exceptions.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [JobFrameworkException()](#jobframeworkexception) | Initializes a new instance of the JobFrameworkException class.
| [JobFrameworkException](#jobframeworkexceptionobject)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of the JobFrameworkException class with values for placeholders in the error message.
| [JobFrameworkException](#jobframeworkexceptionobject--object)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of the JobFrameworkException class with values for placeholders in the error and cause messages.
| [JobFrameworkException](#jobframeworkexceptionobject--object--object--int32)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the JobFrameworkException class with values for placeholders in the error, cause and recovery messages.

### JobFrameworkException()

Initializes a new instance of the JobFrameworkException class.

```cs
JobFrameworkException()
```

### JobFrameworkException([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of the JobFrameworkException class with values for placeholders in the error message.

```cs
JobFrameworkException(Object[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | errorRepl | An array with the values for the error message placeholders.

### JobFrameworkException([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of the JobFrameworkException class with values for placeholders in the error and cause messages.

```cs
JobFrameworkException(Object[], Object[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | errorRepl | An array with the values for the error message placeholders.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | causeRepl | An array with the values for the cause message placeholders.

### JobFrameworkException([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the JobFrameworkException class with values for placeholders in the error, cause and recovery messages.

```cs
JobFrameworkException(Object[], Object[], Object[], Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | errorRepl | An array with the values for the error message placeholders.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | causeRepl | An array with the values for the cause message placeholders.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | recoveryRepl | An array with the values for the recover message placeholders.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | priority | The priority of the exception in the job log. Defaults to 30.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets the processed error message of the exception. |
