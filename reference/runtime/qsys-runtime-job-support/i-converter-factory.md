---
title: "IConverterFactory interface   | QSYS API Reference Guide"
description: "Defines the functionality to create an object that implements the IConverter interface. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the functionality to create an object that implements the IConverter interface.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [GetConverter](#iconverter-getconverterint-ccsid)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a converter for the specified CCSID.
| [SupportsCcsid](#bool-supportsccsidint-ccsid)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Determines if the ICoverter object supports a particular EBCDIC CCSID.

### IConverter GetConverter([int ccsid](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a converter for the specified CCSID.

```cs
IConverter GetConverter(int ccsid)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ccsid | The desired converter's coded character set identifier.

#### Returns

| Type | Description
| --- | ---
| [IConverter](/reference/runtime/qsys-runtime-job-support/i-converter.html) | The converted for the requested CCSID.

### bool SupportsCcsid([int ccsid](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Determines if the ICoverter object supports a particular EBCDIC CCSID.

```cs
bool SupportsCcsid(int ccsid)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ccsid | The coded character set identifier.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the ccsid is supported.
