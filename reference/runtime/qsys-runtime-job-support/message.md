---
title: "Message class                 | QSYS API Reference Guide"
description: "Represent a message sent by a program. "
last_modified_at: 2024-08-09T17:25:29Z
---

Represent a message sent by a program.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Message](#messagestring-string-string-messagetype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Initializes a new instance of the Message class using the specified message id and data from a message file and type.
| [Message](#messagestring-messagetype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Initializes a new instance of the Message class using a text string and type.

### Message([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Initializes a new instance of the Message class using the specified message id and data from a message file and type.

```cs
Message(String, String, String, MessageType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgId | The message identification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgDta | The replacement text, if any, for the message placeholders.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgFile | The message file name where the message description is to be found.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

### Message([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Initializes a new instance of the Message class using a text string and type.

```cs
Message(String, MessageType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The user provide text of the message.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | type | One of the enumeration values that specifies the severity of the message.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Data | Gets the replacement data associated with the message. |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | DateTimeSent | Gets the DateTime when the message was created. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Id | Gets the message identification. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Key | Gets the unique identifier of the message. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MessageFile | Gets the name of the file where the message description can be found. |
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MessageType | Gets the MessageType of the message. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets the text used when the message was created. |
