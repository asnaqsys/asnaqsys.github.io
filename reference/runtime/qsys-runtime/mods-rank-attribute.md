---
title: "MODSRankAttribute class       | QSYS API Reference Guide"
description: "A non-RPG class may be stamped with this attribute to indicate a consumer RPG program to consider it as a Multiple Occurrence Data Structure with the "
last_modified_at: 2024-08-09T16:18:25Z
---

A non-RPG class may be stamped with this attribute to indicate a consumer RPG program to consider it as a Multiple Occurrence Data Structure with the rank
indicated in this attribute.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [MODSRankAttribute](#modsrankattributeint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a MODSRankAttribute object. Describes an item as a multidimensional data structure.

### MODSRankAttribute([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a MODSRankAttribute object. Describes an item as a multidimensional data structure.

```cs
MODSRankAttribute(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rank | Rank of the multidimensional data structure.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Rank | Gets the rank of the multidimensional data structure. |
