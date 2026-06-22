---
title: "dgException Constructors"
description: "Initializes a new instance of the dgException class."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the dgException class.

## Overloads

| Name | Description |
| --- | --- |
| [dgException](#dgexception)() | Initializes a new instance of the dgException class. |
| [dgException](#dgexception-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the dgException class with a specified error message. |
| [dgException](#dgexception-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the dgException class with a specified error message and a reference to the inner exception that is the cause of this exception. |
| [dgException](#dgexception-dgerrornumber-int32-dgerrorclass-string-string-exception)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Create a dgException with the passed error code, system error code,error class, and text. |
| [dgException](#dgexception-dgerrornumber-int32-dgerrorclass-string-string)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a dgException with the passed error code, system error code,error class, and text. |
| [dgException](#dgexception-dgerrornumber)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html)) | Create a dgException with the passed error code. |
| [dgException](#dgexception-dgerrornumber-exception)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Create a dgException with the passed error code and exception. |

<a id="dgexception"></a>
### dgException()

Initializes a new instance of the dgException class.

```cs
dgException()
```

<a id="dgexception-string"></a>
### dgException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the dgException class with a specified error message.

```cs
dgException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The message that describes the error.

<a id="dgexception-string-exception"></a>
### dgException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the dgException class with a specified error message and a reference to the inner exception that is the cause of this exception.

```cs
dgException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message that explains the reason for the exception.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.

<a id="dgexception-dgerrornumber-int32-dgerrorclass-string-string-exception"></a>
### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.

```cs
dgException(dgErrorNumber, Int32, dgErrorClass, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | systemError | The system error code.
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | errorClass | The class of the error.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The error text.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The inner exception.

<a id="dgexception-dgerrornumber-int32-dgerrorclass-string-string"></a>
### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.

```cs
dgException(dgErrorNumber, Int32, dgErrorClass, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | systemError | The system error code.
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | errorClass | The class of the error.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The error text.

<a id="dgexception-dgerrornumber"></a>
### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html))

Create a dgException with the passed error code.

```cs
dgException(dgErrorNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.

<a id="dgexception-dgerrornumber-exception"></a>
### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Create a dgException with the passed error code and exception.

```cs
dgException(dgErrorNumber, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | The Exception object.

## See Also
- [dgException class](dg-exception.html)
