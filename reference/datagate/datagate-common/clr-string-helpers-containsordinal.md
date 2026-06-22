---
title: "ClrStringHelpers.ContainsOrdinal Method"
description: "Determines whether a character is in the current string, using ordinal comparison."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether a character is in the current string, using ordinal comparison.

## Overloads

| Signature | Description |
| --- | --- |
| [ContainsOrdinal](#bool-containsordinal-string-this-char-value)(bool ContainsOrdinal(string This, char value)) | Determines whether a character is in the current string, using ordinal comparison. |
| [ContainsOrdinal](#bool-containsordinal-string-this-string-value)(bool ContainsOrdinal(string This, string value)) | Determines whether a string is in the current string, using ordinal comparison. |

<a id="bool-containsordinal-string-this-char-value"></a>
## bool ContainsOrdinal(string This, char value)

Determines whether a character is in the current string, using ordinal comparison.

```cs
bool ContainsOrdinal(string This, char value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string to search.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | The character to seek.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the value parameter occurs within this string, or if value is the empty string (""); otherwise, false.

<a id="bool-containsordinal-string-this-string-value"></a>
## bool ContainsOrdinal(string This, string value)

Determines whether a string is in the current string, using ordinal comparison.

```cs
bool ContainsOrdinal(string This, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string to search.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The string to seek.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the value parameter occurs within this string, or if value is the empty string (""); otherwise, false.

## See Also
- [ClrStringHelpers class](clr-string-helpers.html)
