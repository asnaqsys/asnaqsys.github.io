---
title: "ActivationGroupAttribute class"
description: "Defines the Activation Group Attribute used to mark a program or service program class. "
last_modified_at: 2024-08-08T21:41:46Z
---

Defines the Activation Group Attribute used to mark a program or service program class.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ActivationGroupAttribute](#activationgroupattributestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the ActivationGroupAttribute class using the supplied group name.
| [ActivationGroupAttribute()](#activationgroupattribute) | Initialize a new instance of the ActivationGroupAttribute class using the default activation group.

### ActivationGroupAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the ActivationGroupAttribute class using the supplied group name.

```cs
ActivationGroupAttribute(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | groupName | The user provided name of the activation group or one of the special values: "*CALLER", "*DFTACTGRP" or "*NEW".  

### ActivationGroupAttribute()

Initialize a new instance of the ActivationGroupAttribute class using the default activation group.

```cs
ActivationGroupAttribute()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Caller | Defines the constant "*CALLER". |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Default | Defines the constant "*DFTACTGRP". |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Eligible | Defines the constant "*ELIGIBLE". |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | GroupName | Gets the name of the activation group. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsCaller | Gets a value that indicates whether the activation group attribute is the special value *CALLER. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsDefault | Gets a value that indicates whether the activation group attribute is the special value *DFTACTGRP. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsNew | Gets a value that indicates whether the activation group attribute is the special value *NEW. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | New | Defines the constant "*NEW". |
