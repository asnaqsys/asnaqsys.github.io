---
title: "HexMethods class              | QSYS API Reference Guide"
description: "Contains extension methods for handling RPG conversions between character strings and their hexadecimal representation. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling RPG conversions between character strings and their hexadecimal representation.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ToHexFromString](#byte--tohexfromstringstring-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | ToHexFromString summary.
| [ToStringFromHex](#string-tostringfromhexbyte--value)([Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | ToStringFromHex summary.

### Byte\[\] ToHexFromString([string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

ToHexFromString summary.

```cs
Byte[] ToHexFromString(string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | ToHexFromString value param.

#### Returns

| Type | Description
| --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | ToHexFromString returns.

### string ToStringFromHex([Byte\[\] value](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

ToStringFromHex summary.

```cs
string ToStringFromHex(Byte[] value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | value | ToStringFromHex value param.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ToStringFromHex returns.
