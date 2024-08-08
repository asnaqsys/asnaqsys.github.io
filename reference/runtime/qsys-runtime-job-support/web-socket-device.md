---
title: "WebSocketDevice class         | QSYS API Reference Guide"
description: "Implements a WebDevice using a socket to communicate with a website for its UI services. "
last_modified_at: 2024-08-08T21:41:46Z
---

Implements a WebDevice using a socket to communicate with a website for its UI services.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [WebDevice](/reference/runtime/qsys-runtime-job-support/web-device.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [WebSocketDevice](#websocketdeviceinteractivejob)([InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html)) | Initializes a new instance of the WebSocketDevice class for a job.

### WebSocketDevice([InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html))

Initializes a new instance of the WebSocketDevice class for a job.

```cs
WebSocketDevice(InteractiveJob)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html) | job | The job associated with the WebSocketDevice.

## Methods

| Signature | Description |
| --- | --- |
| [close()](#void-close) | Closes the device and the assoiated socket.
| [open()](#void-open) | Opens the device.
| [read()](#void-read) | Waits for the user to enter new data on the web site.
| [RiseAbnormalEnd](#void-riseabnormalendstring-abendmessage-string-abendstack)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Marks the device as being in a job that is ending abnormally.
| [sendHostResult()](#void-sendhostresult) | Send the active display file's host service results and waits for new input.
| [SetSocket](#void-setsocketsocket-socket)([Socket](https://learn.microsoft.com/en-us/dotnet/api/system.net.sockets.socket?view=net-8.0)) | Sets the socket used to communicate with the website providing the UI services.

### void close()

Closes the device and the assoiated socket.

```cs
void close()
```

### void open()

Opens the device.

```cs
void open()
```

### void read()

Waits for the user to enter new data on the web site.

```cs
void read()
```

### void RiseAbnormalEnd([string abEndMessage](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string abEndStack](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Marks the device as being in a job that is ending abnormally.

```cs
void RiseAbnormalEnd(string abEndMessage, string abEndStack)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | abEndMessage | A message text describing the abnormal termination.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | abEndStack | The execution stack at the moment of failure.

### void sendHostResult()

Send the active display file's host service results and waits for new input.

```cs
void sendHostResult()
```

### void SetSocket([Socket socket](https://learn.microsoft.com/en-us/dotnet/api/system.net.sockets.socket?view=net-8.0))

Sets the socket used to communicate with the website providing the UI services.

```cs
void SetSocket(Socket socket)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Socket](https://learn.microsoft.com/en-us/dotnet/api/system.net.sockets.socket?view=net-8.0) | socket | The socket used in communications with the website.
