---
title: "WebDevice class               | QSYS API Reference Guide"
description: "Defines the core behavior of the device handling the user interface for an interactive job and provides a base for derived classes. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the core behavior of the device handling the user interface for an interactive job and provides a base for derived classes.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [WebDevice](#webdeviceinteractivejob)([InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html)) | Called from constructors in derived classes to initialize the WebDevice class.

### WebDevice([InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html))

Called from constructors in derived classes to initialize the WebDevice class.

```cs
WebDevice(InteractiveJob)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html) | job | The job owning the device.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | ActiveDisplayFile | Gets the active display file performing the current operation on the device. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DeviceIsOpen | Indicates that the device is open. |

## Methods

| Signature | Description |
| --- | --- |
| [Attach](#void-attachstring-sharefilename-webdisplayfile-displayfile)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html)) | Associates a named display file to this device for future sharing.  Remembers the display file name for potential future sharing.
| [Attach](#void-attachwebdisplayfile-displayfile)([WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html)) | Associates a display file to this device.
| [close()](#void-close) | When overridden in a derived class, closes this device.
| [Detach](#void-detachstring-sharefilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes the association of a named display file with the device.
| [Detach](#void-detachwebdisplayfile-displayfile)([WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html)) | Removes the association of a display file with the device. 
| [Dispose()](#void-dispose) | Calls the close method on the device.
| [GetSharedFile](#webdisplayfile-getsharedfilestring-sharefilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a display file attached to the device.
| [open()](#void-open) | When overridden in a derived class, opens this device.
| [read()](#void-read) | When overridden in a derived class, waits for the user to enter new data on the device's screen.
| [Read](#void-readwebdisplayfile-dspfile)([WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html)) | Present a screen waiting for data to be ready and reads it. 
| [RiseAbnormalEnd](#void-riseabnormalendstring-abendmessage-string-abendstack)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Marks the device as being in a job that is ending abnormally.
| [sendHostResult()](#void-sendhostresult) | When ovveridden in a derived class, sends the host service results in the active display file and waits for new input.
| [SendHostResult](#void-sendhostresultwebdisplayfile-dspfile)([WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html)) | Send the host service results in a display file and waits for new input.
| [SignalDataReadyForProgram()](#void-signaldatareadyforprogram) | Signals the fact that data is now available to the program so it can continue execution.
| [SignalDataReadyForUser()](#void-signaldatareadyforuser) | Signals the fact that data is now available to the user.
| [WaitForDataForProgram()](#void-waitfordataforprogram) | Waits for data to be available for the program.
| [WaitForDataForUser()](#void-waitfordataforuser) | Waits for data to be available for the user.

### void Attach([string shareFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [WebDisplayFile displayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html))

Associates a named display file to this device for future sharing.  Remembers the display file name for potential future sharing.

```cs
void Attach(string shareFileName, WebDisplayFile displayFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareFileName | Shared file name to remember along with the display file.
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | displayFile | The display file being associated to this device.

### void Attach([WebDisplayFile displayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html))

Associates a display file to this device.

```cs
void Attach(WebDisplayFile displayFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | displayFile | The display file being associated to this device.

### void close()

When overridden in a derived class, closes this device.

```cs
void close()
```

### void Detach([string shareFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes the association of a named display file with the device.

```cs
void Detach(string shareFileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareFileName | The name of the display file to be dissociated  from the device.

### void Detach([WebDisplayFile displayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html))

Removes the association of a display file with the device. 

```cs
void Detach(WebDisplayFile displayFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | displayFile | The display file to be dissociated  from the device.

### void Dispose()

Calls the close method on the device.

```cs
void Dispose()
```

### WebDisplayFile GetSharedFile([string shareFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a display file attached to the device.

```cs
WebDisplayFile GetSharedFile(string shareFileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareFileName | The shared name of display file being sought.

#### Returns

| Type | Description
| --- | ---
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | The attached display file. Null if there is no display file with the name seeked. 

### void open()

When overridden in a derived class, opens this device.

```cs
void open()
```

### void read()

When overridden in a derived class, waits for the user to enter new data on the device's screen.

```cs
void read()
```

### void Read([WebDisplayFile dspFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html))

Present a screen waiting for data to be ready and reads it. 

```cs
void Read(WebDisplayFile dspFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | dspFile | The display file to present to the user. It becomes the active display file on the device.

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

When ovveridden in a derived class, sends the host service results in the active display file and waits for new input.

```cs
void sendHostResult()
```

### void SendHostResult([WebDisplayFile dspFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html))

Send the host service results in a display file and waits for new input.

```cs
void SendHostResult(WebDisplayFile dspFile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | dspFile | The display file with host results. It becomes the active display file on the device.

### void SignalDataReadyForProgram()

Signals the fact that data is now available to the program so it can continue execution.

```cs
void SignalDataReadyForProgram()
```

### void SignalDataReadyForUser()

Signals the fact that data is now available to the user.

```cs
void SignalDataReadyForUser()
```

### void WaitForDataForProgram()

Waits for data to be available for the program.

```cs
void WaitForDataForProgram()
```

### void WaitForDataForUser()

Waits for data to be available for the user.

```cs
void WaitForDataForUser()
```
