---
title: "VaryingLengthFieldAttribute class"
description: "A non-RPG class may stamp a property or field member with this attribute to be considered as a varying length field by a consumer RPG program. "
last_modified_at: 2024-08-08T21:41:46Z
---

A non-RPG class may stamp a property or field member with this attribute to be considered as a varying length field by a consumer RPG program.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [VaryingLengthFieldAttribute](#varyinglengthfieldattributestring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a VaryingLengthFieldAttribute object. Describes the item as a fixed-size string with varying length.

### VaryingLengthFieldAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a VaryingLengthFieldAttribute object. Describes the item as a fixed-size string with varying length.

```cs
VaryingLengthFieldAttribute(String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | funcName | The name of the field that contains the current length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxLength | The maximum length of the field.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FunctionName | Gets the name of the associated current length field. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MaxLength | Gets the maximum length. |
