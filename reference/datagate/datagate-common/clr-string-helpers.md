---
title: "ClrStringHelpers class        | QSYS API Reference Guide"
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
| [ContainsInvariantIgnoreCase](#bool-containsinvariantignorecasestring-this-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether a string is in the current string, using invariant culture and ignoring case.
| [ContainsOrdinal](#bool-containsordinalstring-this-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Determines whether a character is in the current string, using ordinal comparison.
| [ContainsOrdinal](#bool-containsordinalstring-this-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether a string is in the current string, using ordinal comparison.
| [ContainsOrdinalIgnoreCase](#bool-containsordinalignorecasestring-this-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Determines whether a character is in the current string, using ordinal comparison and ignoring case.
| [ContainsOrdinalIgnoreCase](#bool-containsordinalignorecasestring-this-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether a string is in the current string, using invariant culture and ignoring case.
| [GetHashCodeCurrentCultureIgnoreCase](#int-gethashcodecurrentcultureignorecasestring-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the current culture and ignoring case.
| [GetHashCodeInvariantCultureIgnoreCase](#int-gethashcodeinvariantcultureignorecasestring-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the invariant culture and ignoring case.
| [GetHashCodeOrdinal](#int-gethashcodeordinalstring-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the specified string comparison.
| [GetHashCodeOrdinalIgnoreCase](#int-gethashcodeordinalignorecasestring-this)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the hash code for this string using the specified string comparison, ignoring case.
| [IndexOfOrdinal](#int-indexofordinalstring-this-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Reports the zero-based index of the first occurrence of the specified character in the current string, using ordinal comparison.
| [ReplaceOrdinal](#string-replaceordinalstring-this-string-oldvalue-string-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison.
| [ReplaceOrdinalIgnoreCase](#string-replaceordinalignorecasestring-this-string-oldvalue-string-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison and ignoring case.

### bool ContainsInvariantIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

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

### bool ContainsOrdinal([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

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

### bool ContainsOrdinal([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

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

### bool ContainsOrdinalIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Determines whether a character is in the current string, using ordinal comparison and ignoring case.

```cs
bool ContainsOrdinalIgnoreCase(string This, char value)
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

### bool ContainsOrdinalIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether a string is in the current string, using invariant culture and ignoring case.

```cs
bool ContainsOrdinalIgnoreCase(string This, string value)
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

### int GetHashCodeCurrentCultureIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the hash code for this string using the current culture and ignoring case.

```cs
int GetHashCodeCurrentCultureIgnoreCase(string This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string for which the hash code is to be obtained.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The hash code for this string, using the current culture and ignoring case.

### int GetHashCodeInvariantCultureIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the hash code for this string using the invariant culture and ignoring case.

```cs
int GetHashCodeInvariantCultureIgnoreCase(string This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string for which the hash code is to be obtained.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The hash code for this string, using the invariant culture and ignoring case.

### int GetHashCodeOrdinal([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the hash code for this string using the specified string comparison.

```cs
int GetHashCodeOrdinal(string This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string for which the hash code is to be obtained.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The hash code for this string.

### int GetHashCodeOrdinalIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the hash code for this string using the specified string comparison, ignoring case.

```cs
int GetHashCodeOrdinalIgnoreCase(string This)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | This | The string for which the hash code is to be obtained.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The hash code for this string, ignoring case.

### int IndexOfOrdinal([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

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

### string ReplaceOrdinal([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string oldValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Returns a new string in which all occurrences of a specified string in the current instance are replaced with another specified string, using ordinal comparison.

```cs
string ReplaceOrdinal(string This, string oldValue, string newValue)
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

### string ReplaceOrdinalIgnoreCase([string This](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string oldValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

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
