---
title: "FixedStringComparer class     | QSYS API Reference Guide"
description: "Provides a comparer for fixed-length strings, allowing for consistent comparison of strings with fixed lengths. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides a comparer for fixed-length strings, allowing for consistent comparison of strings with fixed lengths.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Compare](#int-comparestring-x-string-y)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Compares two strings following Fixed String rules.

### int Compare([string x](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string y](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Compares two strings following Fixed String rules.

```cs
int Compare(string x, string y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | x | First string to compare.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | y | Second string to compare.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A signed number indicating the relative values the two compared values.
