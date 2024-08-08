---
title: "CodePage class                | QSYS API Reference Guide"
description: "Provides facilities to probe an IBM i file&#39;s code page. "
last_modified_at: 2024-08-08T21:41:46Z
---

Provides facilities to probe an IBM i file's code page.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StarHex | Constant representing an unecoded hexadecimal code. |

## Methods

| Signature | Description |
| --- | --- |
| [GetFileCCSIDAttr](#decimal-getfileccsidattradgconnection-dbconnection-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the coded character set identifier of an IBM i physical file.
| [GetFileCCSIDAttr](#decimal-getfileccsidattradgconnection-dbconnection-string-library-string-filename)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the coded character set identifier of an IBM i physical file.
| [IbmCodepageToWinCodepage](#int-ibmcodepagetowincodepageint-codepage)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert an encoded character set identifier to a Windows code page.

### decimal GetFileCCSIDAttr([AdgConnection dbConnection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the coded character set identifier of an IBM i physical file.

```cs
decimal GetFileCCSIDAttr(AdgConnection dbConnection, string pathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | dbConnection | Database connection opened to an IBM i DataGate server.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Qualified named of the physical file.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The file's coded character set identifier.

### decimal GetFileCCSIDAttr([AdgConnection dbConnection](/reference/datagate/datagate-client/adg-connection.html), [string library](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string filename](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the coded character set identifier of an IBM i physical file.

```cs
decimal GetFileCCSIDAttr(AdgConnection dbConnection, string library, string filename)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | dbConnection | Database connection opened to an IBM i DataGate server.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | Name of the file's library.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filename | Name of physical file.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The file's coded character set identifier.

### int IbmCodepageToWinCodepage([int codePage](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert an encoded character set identifier to a Windows code page.

```cs
int IbmCodepageToWinCodepage(int codePage)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | codePage | The IBM code page.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The corresponding Windows code page.
