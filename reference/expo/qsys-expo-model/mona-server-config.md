---
title: "MonaServerConfig class        | QSYS API Reference Guide"
description: "Provides Mona-Server Configuration functionality. "
last_modified_at: 2024-08-09T16:18:58Z
---

Provides Mona-Server Configuration functionality.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

Implements the [IMonaServerConfig Interface](/reference/expo/qsys-expo-model/i-mona-server-config.html), allowing the Website to add [MonaServer](/reference/expo/qsys-expo-model/mona-server-config.html) as a service during the Website Startup [Dependency injection](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection).

## Constructors

| Name | Description |
| --- | --- |
| [MonaServerConfig()](#monaserverconfig) | Initializes new instance of MonaServerConfig class.

### MonaServerConfig()

Initializes new instance of MonaServerConfig class.

```cs
MonaServerConfig()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | AssemblyList | Gets or sets a value that lists the assemblies that are part of this application. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HostName | Gets or sets a value that indicates the Name of the Host. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | JobIdleTimeout | Gets or sets a value that indicates the number of minutes a Job may remain idle before it is shutdown. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Port | Gets or sets a value that indicates the IP Port to use. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | TraceOption | Gets or sets a value that indicates the type of tracing. |
