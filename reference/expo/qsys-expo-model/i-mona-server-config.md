---
title: "IMonaServerConfig interface   | QSYS API Reference Guide"
description: "Exposes MonaServerConfig properties. "
last_modified_at: 2024-08-09T17:26:04Z
---

Exposes MonaServerConfig properties.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>


## Remarks

Website Applications using `ASNA.QSys.Expo` assembly, typically have a configuration file at the root folder of the site named: `appsettings.json`.

The configuration file `appsettings.json` uses [JSON](https://www.json.org/json-en.html) file format.

There is a `"MonaServer"` object defined in the schema for `appsettings.json`, where the Properties described by this class can be set to configure [MonaServer](the Application Server). 


## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | AssemblyList | Gets or sets a value that lists the assemblies that are part of this application. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HostName | Gets or sets HostName as a string. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | JobIdleTimeout | Gets or sets a value that indicates the number of minutes a Job may remain idle before it is shutdown. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Port | Gets or sets IP Port number. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | TraceOption | Gets or sets a value that indicates the type of tracing. |
