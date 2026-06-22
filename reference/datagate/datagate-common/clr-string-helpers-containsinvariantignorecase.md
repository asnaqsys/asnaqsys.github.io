---
title: "ClrStringHelpers.ContainsInvariantIgnoreCase Method"
description: "Determines whether a string is in the current string, using invariant culture and ignoring case."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether a string is in the current string, using invariant culture and ignoring case.

<a id="bool-containsinvariantignorecase-string-this-string-value"></a>
## bool ContainsInvariantIgnoreCase(string This, string value)

Determines whether a string is in the current string, using invariant culture and ignoring case.

```cs
bool ContainsInvariantIgnoreCase(string This, string value)
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
