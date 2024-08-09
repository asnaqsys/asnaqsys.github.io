---
title: "IConverter interface          | QSYS API Reference Guide"
description: "Defines functionality to perform conversions between EBCDIC and Unicode. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines functionality to perform conversions between EBCDIC and Unicode.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [EbcdicToUnicode](#string-ebcdictounicodebyte--source)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Converts EBCDIC characters in an array to Unicode.
| [EbcdicToUnicode](#string-ebcdictounicodebyte--source-int-offset-int-length)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a portion of an array's EBCDIC characters to Unicode.
| [UnicodeToEbcdic](#byte--unicodetoebcdicstring-source)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a unicode string to the corresponding bytes of the equivalent string in EBCDIC.
| [UnicodeToEbcdic](#void-unicodetoebcdicstring-source-int-charindex-int-charcount-byte--bytes-int-byteindex)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a unicode substring to the corresponding bytes of the equivalent string in EBCDIC.

### string EbcdicToUnicode([Byte\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Converts EBCDIC characters in an array to Unicode.

```cs
string EbcdicToUnicode(Byte[] source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | source | An array of bytes encoding the EBCDIC characters.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The Unicode string.

### string EbcdicToUnicode([Byte\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a portion of an array's EBCDIC characters to Unicode.

```cs
string EbcdicToUnicode(Byte[] source, int offset, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | source | An array of bytes encoding the EBCDIC characters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The zero based offset into the first byte to decode.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Number of bytes to decode.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The Unicode string.

### Byte\[\] UnicodeToEbcdic([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a unicode string to the corresponding bytes of the equivalent string in EBCDIC.

```cs
Byte[] UnicodeToEbcdic(string source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The unicode string to convert.

#### Returns

| Type | Description
| --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | The array of bytes holding the EBCDIC representation.

### void UnicodeToEbcdic([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int charIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int charCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Byte\[\] bytes](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [int byteIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts a unicode substring to the corresponding bytes of the equivalent string in EBCDIC.

```cs
void UnicodeToEbcdic(string source, int charIndex, int charCount, Byte[] bytes, int byteIndex)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The unicode string to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | charIndex | The zero based index to the first character in the unicode string to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | charCount | The number of unicode characters to convert.
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | bytes | The array to receive the bytes of the EBCDIC representation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | byteIndex | The zero based index into the byte array to recevie the EBCDIC representation.
