---
title: "MessageBase class             | QSYS API Reference Guide"
description: "Represents a base class for messages, providing properties and methods for message text, cause, recovery suggestions, and logging functionality. "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a base class for messages, providing properties and methods for message text, cause, recovery suggestions, and logging functionality.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Cause | Gets an explanation of the cause of the message. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Class | Gets the class of the message. |
| [IDictionary\<String, Object\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2) | ExtendedProperties | Gets any additional data items related to the message. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ID | Gets the identification of the message. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets the text of the message. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Priority | Defines the property for the message. Conventionally, this property should have a value between 0 and 99.   |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Recovery | Gets a suggestion on how to recover from the situation that caused the message to be issued. |
| [MessageSource](/reference/runtime/qsys-runtime-job-support/message-source.html) | Source | Gets the message source. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SourceAsString | Gets a friendly string of the message source. |
| [TraceEventType](https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.traceeventtype?view=net-8.0) | Type | Gets the type of of message. |

## Methods

| Signature | Description |
| --- | --- |
| [FriendlySourceName](#string-friendlysourcenamemessagesource-src)([MessageSource](/reference/runtime/qsys-runtime-job-support/message-source.html)) | Produces a friendly string for a message source.
| [Write()](#void-write) | Adds a the message to the default job logger.
| [WriteToLog](#void-writetologijoblogger-log)([IJobLogger](/reference/runtime/qsys-runtime-job-support/i-job-logger.html)) | Adds the message to a logger.

### string FriendlySourceName([MessageSource src](/reference/runtime/qsys-runtime-job-support/message-source.html))

Produces a friendly string for a message source.

```cs
string FriendlySourceName(MessageSource src)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MessageSource](/reference/runtime/qsys-runtime-job-support/message-source.html) | src | The message source.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The friendly name.

### void Write()

Adds a the message to the default job logger.

```cs
void Write()
```

### void WriteToLog([IJobLogger log](/reference/runtime/qsys-runtime-job-support/i-job-logger.html))

Adds the message to a logger.

```cs
void WriteToLog(IJobLogger log)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IJobLogger](/reference/runtime/qsys-runtime-job-support/i-job-logger.html) | log | The logger to receive the message.
