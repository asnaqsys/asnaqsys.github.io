---
title: "DynamicReferenceAttribute class"
description: "Declares an assembly to be used as a dynamic reference, which will be queried at runtime to find CALLD targets. "
last_modified_at: 2024-08-09T16:18:25Z
---

Declares an assembly to be used as a dynamic reference, which will be queried at runtime to find CALLD targets.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DynamicReferenceAttribute](#dynamicreferenceattributestring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a DynamicReferenceAttribute object.

### DynamicReferenceAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a DynamicReferenceAttribute object.

```cs
DynamicReferenceAttribute(String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | assemblyName | Either the assembly name or the path to the dynamic reference.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | index | Number to indicate a relative priority of this assembly when searching for programs.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DynamicAssemblyName | Gets the assembly name or path to the dynamic assembly reference. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Index | Gets the relaive priority of this assembly. |
