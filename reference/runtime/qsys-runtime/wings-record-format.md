---
title: "WingsRecordFormat class       | QSYS API Reference Guide"
description: "Contains functionality to construct the WRF, an XML representation of a file. "
last_modified_at: 2024-08-09T17:25:29Z
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
| [CreateWrfFile](#void-createwrffilestring-displayfilepath-dataset-dataset-dictionary-string-string-formatlevelids-datetime-displayfilelastwritetimeutc-int-ccsid-bool-checkformatlevels)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [Dictionary\<String, String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Create a Wrf file out of dataset and save it in the given path.
| [GetWrfDoc](#xdocument-getwrfdocdataset-dataset-dictionary-string-string-formatlevelids-datetime-displayfilelastwritetimeutc-int-ccsid-bool-checkformatlevels-bool-computesha)([DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [Dictionary\<String, String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0), [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Get the Wings Record Format XML document.
| [LoadDataSet](#void-loaddatasetdataset-ds-string-formatprops-dictionary-2-responseindtemplates-bool-throwonerror)([DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Dictionary`2&](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Create the dataset tables for file whose description comes from a Wrf file.
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

### void CreateWrfFile([string displayFilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DataSet dataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [Dictionary\<string, string\> formatLevelIds](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0), [DateTime displayFileLastWriteTimeUtc](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int ccsid](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkFormatLevels](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Create a Wrf file out of dataset and save it in the given path.

```cs
void CreateWrfFile(string displayFilePath, DataSet dataSet, Dictionary<string, string> formatLevelIds, DateTime displayFileLastWriteTimeUtc, int ccsid, bool checkFormatLevels)
```

### XDocument GetWrfDoc([DataSet dataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [Dictionary\<string, string\> formatLevelIds](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0), [DateTime displayFileLastWriteTimeUtc](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [int ccsid](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool checkFormatLevels](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool computeSha](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Get the Wings Record Format XML document.

```cs
XDocument GetWrfDoc(DataSet dataSet, Dictionary<string, string> formatLevelIds, DateTime displayFileLastWriteTimeUtc, int ccsid, bool checkFormatLevels, bool computeSha)
```

### void LoadDataSet([DataSet ds](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [string formatProps](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Dictionary`2& responseIndTemplates](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0), [bool throwOnError](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Create the dataset tables for file whose description comes from a Wrf file.

```cs
void LoadDataSet(DataSet ds, string formatProps, Dictionary`2& responseIndTemplates, bool throwOnError)
```

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
