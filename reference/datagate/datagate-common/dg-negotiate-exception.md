---
title: "DgNegotiateException class    | QSYS API Reference Guide"
description: "Specialized Exception dealing with DataGate protocol negotiation. "
last_modified_at: 2024-08-09T16:18:40Z
---

Specialized Exception dealing with DataGate protocol negotiation.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DgNegotiateException()](#dgnegotiateexception) | Initializes a new instance of the  class without a specific error message.
| [DgNegotiateException](#dgnegotiateexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with a specific error message.

### DgNegotiateException()

Initializes a new instance of the  class without a specific error message.

```cs
DgNegotiateException()
```

### DgNegotiateException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with a specific error message.

```cs
DgNegotiateException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message that explains the reason for the exception.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets a message that describes the current exception. |
