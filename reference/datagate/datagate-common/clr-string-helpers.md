---
title: "ClrStringHelpers class"
description: "This class offers some abstractions for .NET string functions peculiar to the net core platform (and suggested by CA). "
last_modified_at: 2024-08-09T17:25:07Z
---

This class offers some abstractions for .NET string functions peculiar
to the net core platform (and suggested by CA).

**Namespace:** ASNA.DataGate.Common.Util
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ContainsInvariantIgnoreCase](clr-string-helpers-containsinvariantignorecase.html#bool-containsinvariantignorecase-string-this-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether a string is in the current string, using invariant culture and ignoring case.
| [ContainsOrdinal](clr-string-helpers-containsordinal.html#bool-containsordinal-string-this-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Determines whether a character is in the current string, using ordinal comparison.
| [ContainsOrdinal](clr-string-helpers-containsordinal.html#bool-containsordinal-string-this-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether a string is in the current string, using ordinal comparison.
| [ContainsOrdinalIgnoreCase](clr-string-helpers-containsordinalignorecase.html#bool-containsordinalignorecase-string-this-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Determines whether a character is in the current string, using ordinal comparison and ignoring case.
| [ContainsOrdinalIgnoreCase](clr-string-helpers-containsordinalignorecase.html#bool-containsordinalignorecase-string-this-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether a string is in the current string, using invariant culture and ignoring case.
| [GetHashCodeCurrentCultureIgnoreCase](clr-string-helpers-gethashcodecurrentcultureignorecase.html#int-gethashcodecurrentcultureignorecase-string-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the current culture and ignoring case.
| [GetHashCodeInvariantCultureIgnoreCase](clr-string-helpers-gethashcodeinvariantcultureignorecase.html#int-gethashcodeinvariantcultureignorecase-string-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the invariant culture and ignoring case.
| [GetHashCodeOrdinal](clr-string-helpers-gethashcodeordinal.html#int-gethashcodeordinal-string-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the specified string comparison.
| [GetHashCodeOrdinalIgnoreCase](clr-string-helpers-gethashcodeordinalignorecase.html#int-gethashcodeordinalignorecase-string-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the specified string comparison, ignoring case.
| [IndexOfOrdinal](clr-string-helpers-indexofordinal.html#int-indexofordinal-string-this-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Reports the zero-based index of the first occurrence of the specified character in the current string, using ordinal comparison.
| [ReplaceOrdinal](clr-string-helpers-replaceordinal.html#string-replaceordinal-string-this-string-oldvalue-string-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison.
| [ReplaceOrdinalIgnoreCase](clr-string-helpers-replaceordinalignorecase.html#string-replaceordinalignorecase-string-this-string-oldvalue-string-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison and ignoring case.

