---
title: "AdgConnection.Open Method"
description: "Open a database connection."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

Open a database connection by establishing communication with the database server.

## Overloads

| Signature | Description |
| --- | --- |
| [Open](#void-opencancellationtoken-ct)([CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the database with default options.
| [Open](#void-openopenoptions-openoptions-cancellationtoken-ct)([OpenOptions](/reference/datagate/datagate-providers/open-options.html), [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the database with the specified options.


### void Open([CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens a connection to the database with default options.

#### Remarks
This method is used to transition an **AdgConnection** object to the Open state.  If successful, a new database connection is established.  The characteristics of the new connection may be specified by prior assignment of the `SourceProfile` property, or by specifying a **SourceProfile** object in the `AdgConnection constructor`.

This method opens a connection to the database with default options.

If the connection is already open, it returns immediately.

The ct parameter can be used to request cancellation of the operation. If the operation is canceled, it throws an OperationCanceledException.


```cs
void Open(CancellationToken ct)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | ct | A cancellation token that can be used to cancel the operation.



### void Open([OpenOptions openOptions](/reference/datagate/datagate-providers/open-options.html), [CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens a connection to the database with the specified options.

#### Remarks

This method is used to transition an **AdgConnection** object to the Open state.  If successful, a new database connection is established.  The characteristics of the new connection may be specified by prior assignment of the `SourceProfile` property, or by specifying a **SourceProfile** object in the `AdgConnection constructor`.

This method opens a connection to the database with the specified options.

If the connection is already open, it returns immediately.

The ct parameter can be used to request cancellation of the operation. If the operation is canceled, it throws an OperationCanceledException.


```cs
void Open(OpenOptions openOptions, CancellationToken ct)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [OpenOptions](/reference/datagate/datagate-providers/open-options.html) | openOptions | The options for opening the connection.
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | ct | A cancellation token that can be used to cancel the operation.



## See Also

[AdgConnection Class](adg-connection.html)