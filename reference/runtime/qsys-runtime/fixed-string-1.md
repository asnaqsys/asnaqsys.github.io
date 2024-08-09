---
title: "FixedString<T> struct         | QSYS API Reference Guide"
description: "Holds a fixed-string value with the specified length. "
last_modified_at: 2024-08-09T16:18:25Z
---

Holds a fixed-string value with the specified length.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char) | Item | This indexer. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets the length of the fixed-string. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Value | Gets the value of the fixed-string as a string. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | ValueAsObject | Gets the value of the fixed-string as an object. |

## Methods

| Signature | Description |
| --- | --- |
| [CompareTo](#int-comparetoobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Compares this instance with a specified object returns an integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the specified object.
| [Convert](#ifixedsizetype-string-convertstring-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Convert string to FixedSize string.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether two object instances are equal.
| [GetHashCode()](#int-gethashcode) | Returns the hash code for this instance.
| [IsBlanks()](#bool-isblanks) | Determines if the fixed string is null or whitespace.
| [ToLower()](#string-tolower) | Convert to string Lowercase.
| [ToString()](#string-tostring) | Convert to string.
| [ToUpper()](#string-toupper) | Convert to string Uppercase.
| [Trim()](#string-trim) | Returns the string that results from removing all leading and trailing white-space characters from the current string value.
| [TrimEnd()](#string-trimend) | Returns the string that results from removing all white-space characters from the end of the current string value.
| [TrimStart()](#string-trimstart) | Returns the string that results from removing all white-space characters from the start of the current string value.

### int CompareTo([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Compares this instance with a specified object returns an integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the specified object.

```cs
int CompareTo(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare against.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A 32-bit signed integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the obj parameter.

### IFixedSizeType\<string\> Convert([string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Convert string to FixedSize string.

```cs
IFixedSizeType<string> Convert(string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | Input string value.

#### Returns

| Type | Description
| --- | ---
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | A new FixedSize string of the indicated length.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether two object instances are equal.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to compare against.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is equal to the current object; otherwise, false.

### int GetHashCode()

Returns the hash code for this instance.

```cs
int GetHashCode()
```

### bool IsBlanks()

Determines if the fixed string is null or whitespace.

```cs
bool IsBlanks()
```

### string ToLower()

Convert to string Lowercase.

```cs
string ToLower()
```

### string ToString()

Convert to string.

```cs
string ToString()
```

### string ToUpper()

Convert to string Uppercase.

```cs
string ToUpper()
```

### string Trim()

Returns the string that results from removing all leading and trailing white-space characters from the current string value.

```cs
string Trim()
```

### string TrimEnd()

Returns the string that results from removing all white-space characters from the end of the current string value.

```cs
string TrimEnd()
```

### string TrimStart()

Returns the string that results from removing all white-space characters from the start of the current string value.

```cs
string TrimStart()
```
