---
title: "TextBuff class                | QSYS API Reference Guide"
description: "This is the Buffer for UTF8 files. It attempts to read the encoding preamble, which for  this encoding should be unicode point \uFEFF which is  encode"
last_modified_at: 2024-08-09T16:18:58Z
---

This is the Buffer for UTF8 files.
It attempts to read the encoding preamble, which for 
this encoding should be unicode point \uFEFF which is 
encoded as EF BB BF

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ScanBuff](/reference/expo/qsys-expo-model/scan-buff.html)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [GetString](#string-getstringint-beg-int-end)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Returns the string from the buffer betweenthe given file positions.  This needs to bedone carefully, as the number of charactersis, in general, not equal to (end - beg).
| [NewTextBuff](#textbuff-newtextbuffstream-strm)([Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0)) | TextBuff factory.  Reads the file preambleand returns a TextBuff, LittleEndTextBuff orBigEndTextBuff according to the result.

### string GetString([int beg](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int end](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Returns the string from the buffer betweenthe given file positions.  This needs to bedone carefully, as the number of charactersis, in general, not equal to (end - beg).

```cs
string GetString(int beg, int end)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | beg | Begin filepos
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | end | End filepos

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the sub-string

### TextBuff NewTextBuff([Stream strm](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0))

TextBuff factory.  Reads the file preambleand returns a TextBuff, LittleEndTextBuff orBigEndTextBuff according to the result.

```cs
TextBuff NewTextBuff(Stream strm)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Stream](https://learn.microsoft.com/en-us/dotnet/api/system.io.stream?view=net-8.0) | strm | The underlying stream

#### Returns

| Type | Description
| --- | ---
| [TextBuff](/reference/expo/qsys-expo-model/text-buff.html) | the new buffer
