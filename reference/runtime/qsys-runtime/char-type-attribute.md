---
title: "CharTypeAttribute class       | QSYS API Reference Guide"
description: "A non-RPG class may stamp a string member with this attribute to be considered as a fixed-sized character field by a consumer RPG program. "
last_modified_at: 2024-08-09T16:18:25Z
---

A non-RPG class may stamp a string member with this attribute to be considered as a fixed-sized character field by a consumer RPG program.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CharTypeAttribute](#chartypeattributeint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a CharTypeAttribute object. This attribute describes the implied fixed string length of a string value.

### CharTypeAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a CharTypeAttribute object. This attribute describes the implied fixed string length of a string value.

```cs
CharTypeAttribute(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | The length of this fixed-sized string.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the (fixed) string. |
