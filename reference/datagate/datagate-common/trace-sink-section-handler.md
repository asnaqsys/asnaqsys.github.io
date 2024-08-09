---
title: "TraceSinkSectionHandler class | QSYS API Reference Guide"
description: "Handles the configuration section for trace sinks in the application. Implements the  interface. "
last_modified_at: 2024-08-09T17:25:07Z
---

Handles the configuration section for trace sinks in the application.
Implements the  interface.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [TraceSinkSectionHandler()](#tracesinksectionhandler) | Initializes a new instance of the  class.

### TraceSinkSectionHandler()

Initializes a new instance of the  class.

```cs
TraceSinkSectionHandler()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | AppendValues | Gets a value indicating whether to append values in the trace sink section. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | KeyName | Gets or sets the key name for the trace sink section. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ValueName | Gets or sets the value name for the trace sink section. |

## Methods

| Signature | Description |
| --- | --- |
| [Create](#object-createobject-parent-object-context-xmlnode-section)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0)) | Creates a new instance of the TraceSinkSectionHandler class.

### object Create([object parent](https://docs.microsoft.com/en-us/dotnet/api/system.object), [object context](https://docs.microsoft.com/en-us/dotnet/api/system.object), [XmlNode section](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0))

Creates a new instance of the TraceSinkSectionHandler class.

```cs
object Create(object parent, object context, XmlNode section)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | parent | The parent object.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | context | The context object.
| [XmlNode](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlnode?view=net-8.0) | section | The XML node that contains the configuration information to be handled.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | A new instance of the TraceSinkSectionHandler class.
