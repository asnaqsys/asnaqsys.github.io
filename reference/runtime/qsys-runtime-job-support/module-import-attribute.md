---
title: "ModuleImportAttribute class   | QSYS API Reference Guide"
description: "Attribute to indicate the list of (external) modules this program will contain. "
last_modified_at: 2024-08-08T21:41:46Z
---

Attribute to indicate the list of (external) modules this program will contain.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ModuleImportAttribute](#moduleimportattributetype)([Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Attribute constructor.

### ModuleImportAttribute([Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Attribute constructor.

```cs
ModuleImportAttribute(Type[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type) | types | List of module types this program will contain.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ModuleTypes | Array containing the module types. |
