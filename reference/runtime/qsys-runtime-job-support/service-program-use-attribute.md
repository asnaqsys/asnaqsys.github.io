---
title: "ServiceProgramUseAttribute class"
description: "Attribute to indicate the list of service programs to which a program is bound. "
last_modified_at: 2024-08-09T16:18:25Z
---

Attribute to indicate the list of service programs to which a program is bound.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ServiceProgramUseAttribute](#serviceprogramuseattributetype)([Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Attribute constructor.

### ServiceProgramUseAttribute([Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Attribute constructor.

```cs
ServiceProgramUseAttribute(Type[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type) | types | List of service program types a program is bound to.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Type\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ProgramTypes | Array containing the service program types. |
