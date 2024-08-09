---
title: "WorkstationDataSet class      | QSYS API Reference Guide"
description: "Represents the dataset of a workstation file. "
last_modified_at: 2024-08-09T17:25:29Z
---

Represents the dataset of a workstation file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [MarshalByValueComponent](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.marshalbyvaluecomponent?view=net-8.0) --> [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) --> [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [WorkstationDataSet](#workstationdatasetstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the WorkstationDataSet class.

### WorkstationDataSet([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the WorkstationDataSet class.

```cs
WorkstationDataSet(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | Name of the workstation file field in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatProps | String containing the serialized XML for the record format section of the Wrf file.

## Methods

| Signature | Description |
| --- | --- |
| [GetObjectData](#void-getobjectdataserializationinfo-info-streamingcontext-context)([SerializationInfo](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo?view=net-8.0), [StreamingContext](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext?view=net-8.0)) | Populates a serialization information object with the data needed to serializethe System.Data.DataSet.
| [GetStatus](#wsdsstatus-getstatusdataset-ds)([DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset)) | Gets the WsDs Status value from the property flags in the DataSet.
| [Initialize()](#void-initialize) | Initialize the WorkstationDataSet object. This method skips the 'normal' initializing path and does nothing.The true initialization of the WorkstationDataSet happens when calling InitializeFormats.
| [InitializeFormats()](#void-initializeformats) | Initialize the WorkstationDataSet object.
| [SetStatusFlag](#void-setstatusflagdataset-ds-wsdsstatus-statusflag-bool-turnflagon)([DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [WsDsStatus](/reference/runtime/qsys-runtime/ws-ds-status.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Set the status flag of the dataset to None or Read.

### void GetObjectData([SerializationInfo info](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo?view=net-8.0), [StreamingContext context](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext?view=net-8.0))

Populates a serialization information object with the data needed to serializethe System.Data.DataSet.

```cs
void GetObjectData(SerializationInfo info, StreamingContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SerializationInfo](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.serializationinfo?view=net-8.0) | info | A System.Runtime.Serialization.SerializationInfo that holds the serialized data            associated with the System.Data.DataSet.
| [StreamingContext](https://learn.microsoft.com/en-us/dotnet/api/system.runtime.serialization.streamingcontext?view=net-8.0) | context | A System.Runtime.Serialization.StreamingContext that contains the source and            destination of the serialized stream associated with the System.Data.DataSet.

### WsDsStatus GetStatus([DataSet ds](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset))

Gets the WsDs Status value from the property flags in the DataSet.

```cs
WsDsStatus GetStatus(DataSet ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | ds | Input DataSet.

#### Returns

| Type | Description
| --- | ---
| [WsDsStatus](/reference/runtime/qsys-runtime/ws-ds-status.html) | The WsDs Status.

### void Initialize()

Initialize the WorkstationDataSet object. This method skips the 'normal' initializing path and does nothing.The true initialization of the WorkstationDataSet happens when calling InitializeFormats.

```cs
void Initialize()
```

### void InitializeFormats()

Initialize the WorkstationDataSet object.

```cs
void InitializeFormats()
```

### void SetStatusFlag([DataSet ds](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset), [WsDsStatus statusFlag](/reference/runtime/qsys-runtime/ws-ds-status.html), [bool turnFlagOn](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Set the status flag of the dataset to None or Read.

```cs
void SetStatusFlag(DataSet ds, WsDsStatus statusFlag, bool turnFlagOn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | ds | Dataset whose status is to be set.
| [WsDsStatus](/reference/runtime/qsys-runtime/ws-ds-status.html) | statusFlag | Status flag value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | turnFlagOn | True to set the flag, false to remove it.
