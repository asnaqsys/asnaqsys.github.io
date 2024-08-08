---
title: "IWebDisplayFileProvider interface"
description: "Web Display File Provider Interface. It contains methods to handle all Input and Output operations on the file. "
last_modified_at: 2024-08-08T21:41:46Z
---

Web Display File Provider Interface. It contains methods to handle all Input and Output operations on the file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Attach](#adgdataset-attachidisplayfile-webdisplayfile)([IDisplayFile](/reference/expo/qsys-expo-model/i-display-file.html)) | Attach to DataSet. 
| [GetNewWebDisplayFile](#idisplayfile-getnewwebdisplayfilestring-dclfilename-string-filepath-adgdataset-dataset-bool-bshareopendatapath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Get New Web DisplayFile instance.
| [GetSharedFile](#idisplayfile-getsharedfilestring-dclfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get shared file.

### AdgDataSet Attach([IDisplayFile webDisplayFile](/reference/expo/qsys-expo-model/i-display-file.html))

Attach to DataSet. 

```cs
AdgDataSet Attach(IDisplayFile webDisplayFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDisplayFile](/reference/expo/qsys-expo-model/i-display-file.html) | webDisplayFile | Input Web Displayfile instance.

#### Returns

| Type | Description
| --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | The DataSet.

### IDisplayFile GetNewWebDisplayFile([string DclFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string FilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgDataSet dataSet](/reference/datagate/datagate-client/adg-data-set.html), [bool bShareOpenDataPath](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Get New Web DisplayFile instance.

```cs
IDisplayFile GetNewWebDisplayFile(string DclFileName, string FilePath, AdgDataSet dataSet, bool bShareOpenDataPath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DclFileName | Input declared file name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FilePath | Input file path.
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | dataSet | Input DataSet.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bShareOpenDataPath | True if open data path is shared.

#### Returns

| Type | Description
| --- | ---
| [IDisplayFile](/reference/expo/qsys-expo-model/i-display-file.html) | The DisplayFile instance.

### IDisplayFile GetSharedFile([string DclFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get shared file.

```cs
IDisplayFile GetSharedFile(string DclFileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DclFileName | Input declared file name.

#### Returns

| Type | Description
| --- | ---
| [IDisplayFile](/reference/expo/qsys-expo-model/i-display-file.html) | Display file instance.
