---
title: "ClrStringHelpers.ReplaceOrdinalIgnoreCase Method"
description: "Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison and ignoring case."
---

## Definition

**Namespace:** ASNA.DataGate.Common.Util  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison and ignoring case.

<a id="string-replaceordinalignorecase-string-this-string-oldvalue-string-newvalue"></a>
## string ReplaceOrdinalIgnoreCase(string This, string oldValue, string newValue)

Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison and ignoring case.

```cs
string ReplaceOrdinalIgnoreCase(string This, string oldValue, string newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string performing the replace operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | oldValue | The string to be replaced.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | The string to replace all occurrences of oldValue.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | A string that is equivalent to the current string except that all instances of oldValue are replaced with newValue. If oldValue is not found in the current instance, the method returns the current instance unchanged.

## See Also
- [ClrStringHelpers class](clr-string-helpers.html)
