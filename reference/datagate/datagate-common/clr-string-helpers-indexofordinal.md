---
title: "ClrStringHelpers.IndexOfOrdinal Method"
description: "Reports the zero-based index of the first occurrence of the specified character in the current string, using ordinal comparison."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reports the zero-based index of the first occurrence of the specified character in the current string, using ordinal comparison.

<a id="int-indexofordinal-string-this-char-value"></a>
## int IndexOfOrdinal(string This, char value)

Reports the zero-based index of the first occurrence of the specified character in the current string, using ordinal comparison.

```cs
int IndexOfOrdinal(string This, char value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string to search.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | The character to seek.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The zero-based index position of value if that character is found, or -1 if it is not.

## See Also
- [ClrStringHelpers class](clr-string-helpers.html)
