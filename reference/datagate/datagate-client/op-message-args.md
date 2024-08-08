---
title: "OpMessageArgs class           | QSYS API Reference Guide"
description: "Represents the arguments for an operation message event. This class is derived from EventArgs and is used to pass a message string with an event. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents the arguments for an operation message event.
This class is derived from EventArgs and is used to pass a message string with an event.

**Namespace:** ASNA.DataGate.Client.CopyData
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [EventArgs](https://learn.microsoft.com/en-us/dotnet/api/system.eventargs?view=net-8.0)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [OpMessageArgs](#opmessageargsstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class.

### OpMessageArgs([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class.

```cs
OpMessageArgs(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msg | The message to be passed with the event.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets the message associated with the event. |
