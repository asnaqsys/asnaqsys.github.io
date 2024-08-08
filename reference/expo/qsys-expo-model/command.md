---
title: "Command class                 | QSYS API Reference Guide"
description: "Provides functionality to interact directly with a Job. "
last_modified_at: 2024-08-08T21:42:10Z
---

Provides functionality to interact directly with a Job.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Command](#commandhttpcontext-int32)([HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the Command class for the provided HTTP context and job handle.

### Command([HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the Command class for the provided HTTP context and job handle.

```cs
Command(HttpContext, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0) | HttpContext | The information associated with the HTTP request.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | jobHandle | The identifier of the jobHandle for this command.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [JobSession](/reference/expo/qsys-expo-model/job-session.html) | JobSession | Gets a reference to the JobSession for the Command. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | JobStarted | Gets a value that indicates whether the Job has been started. |

## Methods

| Signature | Description |
| --- | --- |
| [Call](#void-callstring-assemblypath-string-programname-string--parms)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Requests that a program be executed in the Job.  If the program displays a page it will be shown in the browser.
| [Call](#void-callstring-assemblypath-string-programname-string--parms-string-callbackpage)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Requests that a program be executed in the Job.
| [CallSilent](#webdisplayfileproxy-callsilentstring-assemblypath-string-programname-string--parms)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Requests that a program be executed in the Job.  The caller will have to handle any input requested by the program via a display page.
| [CommitJobSession()](#void-commitjobsession) | Store the job session in the data store. 
| [GetActiveDisplayFile()](#webdisplayfileproxy-getactivedisplayfile) | Get the active display file.
| [GetCommandFromRequest](#command-getcommandfromrequesthttpcontext-httpcontext)([HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0)) | Initializes a new instance of the Command class for the provided HTTP context which should contain a JobHandle.
| [GetLdaField](#string-getldafieldint-start-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the value stored in the Job's Local Data Area.
| [GetLdcObject](#string-getldcobjectstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value from the Job's Local Data Collection associated with the specified name.
| [GetRequestJobHandle](#int-getrequestjobhandlehttpcontext-httpcontext-displaypagesoptions-dpoptions)([HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0), [DisplayPagesOptions](/reference/expo/qsys-expo-model/display-pages-options.html)) | Get the JobHandle for the Request in the HttpContext.
| [PushEndRequest()](#void-pushendrequest) | Invokes the EndRequest operation on the waiting blue thread program.
| [PushKeyFocus](#webdisplayfileproxy-pushkeyfocusaidkeyibm-key-short-virtualrowcol-string-fieldname)([AidKeyIBM](/reference/expo/qsys-expo-model/aid-key-ibm.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Provides input to the blue thread program waiting for input.
| [RemoveLdcObject](#void-removeldcobjectstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes the element from the Job's Local Data Collection with the specified key. Removing an element increments the version of the LocalDataCollection.
| [RequestShutdown()](#void-requestshutdown) | Send a request to the Job to terminate its processing.
| [Return](#void-returnstring-result)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Informs the Job that it should return to program execution.
| [SetLdaField](#void-setldafieldint-start-int-length-string-newvalue)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Stores a value in the Job's Local Data Area.
| [SetLdcObject](#void-setldcobjectstring-name-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds or updates an element of the Job's Local Data Collection with the specified key. Adding an element increments the Local Data Collection version.
| [StartJob()](#int-startjob) | Starts a new Job.

### void Call([string assemblyPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string programName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] parms](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Requests that a program be executed in the Job.  If the program displays a page it will be shown in the browser.

```cs
void Call(string assemblyPath, string programName, String[] parms)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | assemblyPath | The path to the assembly.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The fully qualified program name to be call.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parms | An array of parameters to be passed. Only strings can be passed.

### void Call([string assemblyPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string programName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] parms](https://docs.microsoft.com/en-us/dotnet/api/system.string), [string callbackPage](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Requests that a program be executed in the Job.

```cs
void Call(string assemblyPath, string programName, String[] parms, string callbackPage)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | assemblyPath | The path to the assembly.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The fully qualified program name to be call.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parms | An array of parameters to be passed. Only strings can be passed.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | callbackPage | The URL, or route to the page, to transfer to after the call finishes.

### WebDisplayFileProxy CallSilent([string assemblyPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string programName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] parms](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Requests that a program be executed in the Job.  The caller will have to handle any input requested by the program via a display page.

```cs
WebDisplayFileProxy CallSilent(string assemblyPath, string programName, String[] parms)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | assemblyPath | The path to the assembly.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | The fully qualified program name to be call.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parms | An array of parameters to be passed. Only strings can be passed.

#### Returns

| Type | Description
| --- | ---
| [WebDisplayFileProxy](/reference/expo/qsys-expo-model/web-display-file-proxy.html) | 

### void CommitJobSession()

Store the job session in the data store. 

```cs
void CommitJobSession()
```

### WebDisplayFileProxy GetActiveDisplayFile()

Get the active display file.

```cs
WebDisplayFileProxy GetActiveDisplayFile()
```

### Command GetCommandFromRequest([HttpContext HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0))

Initializes a new instance of the Command class for the provided HTTP context which should contain a JobHandle.

```cs
Command GetCommandFromRequest(HttpContext HttpContext)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0) | HttpContext | The information associated with the HTTP request. Request should have a JobHandle in the QueryString or the Form.

#### Returns

| Type | Description
| --- | ---
| [Command](/reference/expo/qsys-expo-model/command.html) | A Command instance associated with the JobHandle.

### string GetLdaField([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the value stored in the Job's Local Data Area.

```cs
string GetLdaField(int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where the value is stored.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The requested field value.

### string GetLdcObject([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the value from the Job's Local Data Collection associated with the specified name.

```cs
string GetLdcObject(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name whose value to get.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value associated with the specified name.

### int GetRequestJobHandle([HttpContext httpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0), [DisplayPagesOptions dpOptions](/reference/expo/qsys-expo-model/display-pages-options.html))

Get the JobHandle for the Request in the HttpContext.

```cs
int GetRequestJobHandle(HttpContext httpContext, DisplayPagesOptions dpOptions)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0) | httpContext | The current HttpContext.
| [DisplayPagesOptions](/reference/expo/qsys-expo-model/display-pages-options.html) | dpOptions | The website's DisplayPage options, default's to the configured options.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The JobHandle found in the HttpContext Request's QueryOption or Form.

### void PushEndRequest()

Invokes the EndRequest operation on the waiting blue thread program.

```cs
void PushEndRequest()
```

### WebDisplayFileProxy PushKeyFocus([AidKeyIBM key](/reference/expo/qsys-expo-model/aid-key-ibm.html), [short virtualRowCol](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string fieldName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Provides input to the blue thread program waiting for input.

```cs
WebDisplayFileProxy PushKeyFocus(AidKeyIBM key, short virtualRowCol, string fieldName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AidKeyIBM](/reference/expo/qsys-expo-model/aid-key-ibm.html) | key | The enumeration value defining the key the program would think was "pressed" by the user.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | virtualRowCol | The virtual row and column of the control with focus when the key was "pressed".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldName | The field name of the control with focus when the key was "pressed".

#### Returns

| Type | Description
| --- | ---
| [WebDisplayFileProxy](/reference/expo/qsys-expo-model/web-display-file-proxy.html) | The active Display File

### void RemoveLdcObject([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes the element from the Job's Local Data Collection with the specified key. Removing an element increments the version of the LocalDataCollection.

```cs
void RemoveLdcObject(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the element to remove.

### void RequestShutdown()

Send a request to the Job to terminate its processing.

```cs
void RequestShutdown()
```

### void Return([string result](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Informs the Job that it should return to program execution.

```cs
void Return(string result)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | result | The resulting string to be passed back to the Job.

### void SetLdaField([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Stores a value in the Job's Local Data Area.

```cs
void SetLdaField(int start, int length, string newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where newValue will be stored.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to store.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | The string value to store in the LDA.

### void SetLdcObject([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds or updates an element of the Job's Local Data Collection with the specified key. Adding an element increments the Local Data Collection version.

```cs
void SetLdcObject(string name, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name whose value to set.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The value of the element.

### int StartJob()

Starts a new Job.

```cs
int StartJob()
```
