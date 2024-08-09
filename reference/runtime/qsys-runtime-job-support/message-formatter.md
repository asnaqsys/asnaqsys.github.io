---
title: "MessageFormatter class        | QSYS API Reference Guide"
description: "Provides functionality to format a message. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides functionality to format a message.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [FormatMessage](#string-formatmessagestring-msgfilepath-message-message)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Message](/reference/runtime/qsys-runtime-job-support/message.html)) | Produces a string with the formatted first level text for a message. Any placeholders are replaced with values from the message data. 
| [FormatMessageText](#bool-formatmessagetextstring-msgfilepath-message-message-string-firstleveltext-string-secondleveltext)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Message](/reference/runtime/qsys-runtime-job-support/message.html), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Produces the strings with the formatted first and second level text for a message. Any placeholders are replaced with values from the message data. 

### string FormatMessage([string msgFilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Message message](/reference/runtime/qsys-runtime-job-support/message.html))

Produces a string with the formatted first level text for a message. Any placeholders are replaced with values from the message data. 

```cs
string FormatMessage(string msgFilePath, Message message)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msgFilePath | The file path to the message file containing the definition for the message. Use null to take the Job's default message file path.
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | message | The message to be formatted.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The formatted text of the message.

### bool FormatMessageText([string msgFilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Message message](/reference/runtime/qsys-runtime-job-support/message.html), [String& firstLevelText](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String& secondLevelText](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Produces the strings with the formatted first and second level text for a message. Any placeholders are replaced with values from the message data. 

```cs
bool FormatMessageText(string msgFilePath, Message message, String& firstLevelText, String& secondLevelText)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msgFilePath | The file path to the message file containing the definition for the message. Use null to take the Job's default message file path.
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | message | The message to be formatted.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | firstLevelText | The formatted first level text of the message.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | secondLevelText | The formatted second level text of the message.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the message was successfully formatted; otherwise, false.
