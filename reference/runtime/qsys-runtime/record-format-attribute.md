---
title: "RecordFormatAttribute class   | QSYS API Reference Guide"
description: "A non-RPG class may stamp a field with this attribute to be considered as a record format by a consumer RPG program. "
last_modified_at: 2024-08-09T16:18:25Z
---

A non-RPG class may stamp a field with this attribute to be considered as a record format by a consumer RPG program.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RecordFormatAttribute](#recordformatattributestring--string)([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a RecordFormatAttribute object. The attribute describes the records and fields in a database file.

### RecordFormatAttribute([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a RecordFormatAttribute object. The attribute describes the records and fields in a database file.

```cs
RecordFormatAttribute(String[], String[][])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordFormatNames | The record format names.
| [String\[\]\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldsInFormats | The field names in each record format.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String\[\]\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FieldsInFormats | Gets the array of arrays contianing the field names in the record formats. |
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | RecordFormatNames | Gets the record format names. |
