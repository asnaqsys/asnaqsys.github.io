---
title: "DSLengthAttribute class       | QSYS API Reference Guide"
description: "A non-RPG class may be stamped with this attribute to indicate a consumer RPG program to consider it as a Data Structure with the specified length. "
last_modified_at: 2024-08-09T17:25:29Z
---

A non-RPG class may be stamped with this attribute to indicate a consumer RPG program to consider it as a Data Structure with the specified length.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DSLengthAttribute](#dslengthattributeint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a DSLengthAttribute object. Describes the item as a data structure with the given length.

### DSLengthAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a DSLengthAttribute object. Describes the item as a data structure with the given length.

```cs
DSLengthAttribute(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length of the deta structure.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the data structure. |
