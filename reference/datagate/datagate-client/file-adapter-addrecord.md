---
title: "FileAdapter.AddRecord Method"
description: "Adds a record to a file."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

Add a record to a file.

## Overloads

| Signature | Description |
| --- | --- |
| [AddRecord](#void-addrecordadgdataset)( [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Adds a record to the file using the provided AdgDataSet.
| [AddRecord](#void-addrecordxmlreader-adgdataset)( [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Adds a record to the file using the provided XmlReader and AdgDataSet.
| [AddRecord](#void-addrecordadgdataset-char)( [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html), [Char\[ \]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Adds a record to the file using the provided AdgDataSet and application indicators.


## void AddRecord(AdgDataSet)

Adds records to the file using the provided AdgDataSet.

```cs
void AddRecord(AdgDataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.

### Remarks
The AddRecord method is used to add a record to the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the AddRecord method of the FileData object of the FileAdapter, passing the provided AdgDataSet. The AddRecord method of the FileData object adds a record to the file with the data from the AdgDataSet. The AdgDataSet should contain the data for the new record in its tables. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.

## void AddRecord(XmlReader, AdgDataSet)

Add the records provided by an XmlReader to the file.


```cs
void AddRecord(XmlReader, AdgDataSet)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | xr | The XmlReader containing the data for the new record.
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the schema for the new record.

### Remarks

The AddRecord method is used to add a record to the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the AddRecord method of the FileData object of the FileAdapter, passing the provided XmlReader and AdgDataSet. The AddRecord method of the FileData object adds a record to the file with the data from the XmlReader, using the schema from the AdgDataSet. The XmlReader should contain the data for the new record in XML format. The AdgDataSet should contain the schema for the new record. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.


## void AddRecord(AdgDataSet, Char[])

Adds a record to the file using the provided AdgDataSet and application indicators.


```cs
void AddRecord(AdgDataSet ds, Char[] appIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | ds | The AdgDataSet containing the data for the new record.
| [Char[]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | appIndicators | The application indicators for the new record.

### Remarks

The AddRecord method is used to add a record to the file that the FileAdapter is working with. It first checks if the provided AdgDataSet is null. If it is, it throws an ArgumentNullException. It then calls the AddRecord method of the FileData object of the FileAdapter, passing the provided AdgDataSet and application indicators. The AddRecord method of the FileData object adds a record to the file with the data from the AdgDataSet and the specified application indicators. The AdgDataSet should contain the data for the new record in its tables. The application indicators should be an array of characters that indicate the status of the application for the new record. The structure of the AdgDataSet should match the structure of the file that the FileAdapter is working with.


## See Also

[FileAdapter Class](file-adapter.html)
