---
title: "WingsRecordFormat class       | QSYS API Reference Guide"
description: "Contains functionality to construct the WRF, an XML representation of a file. "
last_modified_at: 2024-08-08T21:41:46Z
---

Contains functionality to construct the WRF, an XML representation of a file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ComputeSha](#string-computeshaxelement-layoutelement)([XElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.linq.xelement?view=net-8.0)) | Computes SHA hash value.
| [UpdateWrfFile](#void-updatewrffilestring-displayfilepath-xdocument-wrfdoc)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [XDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.linq.xdocument?view=net-8.0)) | Sign the Wrf file and saves it to disk.

### string ComputeSha([XElement layoutElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.linq.xelement?view=net-8.0))

Computes SHA hash value.

```cs
string ComputeSha(XElement layoutElement)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XElement](https://learn.microsoft.com/en-us/dotnet/api/system.xml.linq.xelement?view=net-8.0) | layoutElement | Input XML element.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The hash value as a string.

### void UpdateWrfFile([string displayFilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [XDocument wrfDoc](https://learn.microsoft.com/en-us/dotnet/api/system.xml.linq.xdocument?view=net-8.0))

Sign the Wrf file and saves it to disk.

```cs
void UpdateWrfFile(string displayFilePath, XDocument wrfDoc)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | displayFilePath | Path to the location where the Wrf file will be saved.
| [XDocument](https://learn.microsoft.com/en-us/dotnet/api/system.xml.linq.xdocument?view=net-8.0) | wrfDoc | XDocument containing the Wrf.
