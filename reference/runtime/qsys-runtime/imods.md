---
title: "IMODS interface               | QSYS API Reference Guide"
description: "Describes the set of operations of a multi-occurrence data structure. "
last_modified_at: 2024-08-08T21:41:46Z
---

Describes the set of operations of a multi-occurrence data structure.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** [IDS](/reference/runtime/qsys-runtime/ids.html)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Occurrence | Gets the indices of the current occurrence of the multi data structure. |

## Methods

| Signature | Description |
| --- | --- |
| [ClearAll()](#void-clearall) | Clears all occurrences of the data structure.
| [DumpAll()](#string-dumpall) | Gets the contents of all occurrences of the multi data structure as a string.
| [LoadAll](#void-loadallstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Copies the given string into the multi-occurrence data structure. 

### void ClearAll()

Clears all occurrences of the data structure.

```cs
void ClearAll()
```

### string DumpAll()

Gets the contents of all occurrences of the multi data structure as a string.

```cs
string DumpAll()
```

### void LoadAll([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Copies the given string into the multi-occurrence data structure. 

```cs
void LoadAll(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to copy.
