---
title: "IWebDisplayFileProvider interface"
description: "Web Display File Provider Interface. It contains methods to handle all Input and Output operations on the file. "
last_modified_at: 2024-08-09T16:18:25Z
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
| [GetWRF](#int-getwrfstring-filepath-int-wrfoptions-int-handlertype-string-formatprops-string-resolvedaspfilepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get Wings Record Format ID.

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

### int GetWRF([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int wrfOptions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int handlerType](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [String& formatProps](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String& resolvedAspFilePath](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Get Wings Record Format ID.

```cs
int GetWRF(string filePath, int wrfOptions, int handlerType, String& formatProps, String& resolvedAspFilePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Input file path.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | wrfOptions | Input Wings Record Format options.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | handlerType | Input handler type.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatProps | Output format properties.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | resolvedAspFilePath | Output resolved as ASP filepath.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The Get Wings Record Format ID.
