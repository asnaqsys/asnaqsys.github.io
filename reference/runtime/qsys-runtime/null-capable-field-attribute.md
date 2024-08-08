---
title: "NullCapableFieldAttribute class"
description: "A non-RPG class may stamp a property or field member with this attribute to be considered as a null capable field by a consumer RPG program. "
last_modified_at: 2024-08-08T21:41:46Z
---

A non-RPG class may stamp a property or field member with this attribute to be considered as a null capable field by a consumer RPG program.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [NullCapableFieldAttribute](#nullcapablefieldattributestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a NullCapableFieldAttribute object. 

### NullCapableFieldAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a NullCapableFieldAttribute object. 

```cs
NullCapableFieldAttribute(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | funcName | Name of the associated boolean field to indicate that this field is null.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FunctionName | Gets the name of the associated boolean field. |
