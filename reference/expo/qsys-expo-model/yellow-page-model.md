---
title: "YellowPageModel class         | QSYS API Reference Guide"
description: "Defines YellowPageModel class and provides a base for the &#39;Yellow&#39; Page Model "
last_modified_at: 2024-08-09T16:18:58Z
---

Defines YellowPageModel class and provides a base for the 'Yellow' Page Model

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [PageModel](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.razorpages.pagemodel?view=aspnetcore-8.0)
<br>
<br>

## Remarks

The [Web & Application Server](/concepts/architecture/application-architecture.html#interactive-job-architecture) components of the Application Architecture have two sub-components that are conveniently identified by the designers with colors: yellow-component and blue-component (basic color theory shows how combining *yellow* and *blue* colors renders *green*). Green *Web & Application Server* are defined by the *Yellow* component plus the *Blue* component.

The `YellowPageModel` is the class that provides the *Yellow* component services in the Web & Application Server](/concepts/architecture/application-architecture.html#interactive-job-architecture).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataSet](https://docs.microsoft.com/en-us/dotnet/api/system.data.dataset) | ActiveDataSet | Gets the Active DataSet for the Active Displayfile |
| [WebDisplayFileProxy](/reference/expo/qsys-expo-model/web-display-file-proxy.html) | ActiveDisplayFile | Gets the Active Web Displayfile |
| [ExpoAjaxRequest](/reference/expo/qsys-expo-model/expo-ajax-request.html) | ajaxReq | Gets or sets a value indicating wether the request context type was application AJAX |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | creatingFakeData | Internal use. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InputDataAvailable | When true, derived class defines that data is available on input |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | JobHandleForBrowser | Gets the handle for the Job's session store when using MultiJobOnBrowser. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | renderingFakeData | Internal use. |
| [SessionStorage](/reference/expo/qsys-expo-model/session-storage.html) | SessionStore | Gets the SessionStorage instance (creates a new one if it does not exist) |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UserDataIsInvalid | Derived class implements to determine if the user input data is valid |

## Methods

| Signature | Description |
| --- | --- |
| [AjaxGetIconCollectionActionResult()](#jsonresult-ajaxgeticoncollectionactionresult) | Gets the JsonResult for a "getIconCollection" AJAX request
| [AjaxGetRecordsActionResult()](#jsonresult-ajaxgetrecordsactionresult) | Gets the JsonResult for a "getRecords" AJAX request
| [ClearModelProperties()](#void-clearmodelproperties) | Derived class implements method to Clear all model properties
| [ClearSubfilesInSession()](#void-clearsubfilesinsession) | Clears cached Session storage entries related to All Subfiles.
| [CommitJobSession()](#void-commitjobsession) | Store the job session in the data store. 
| [DumpModelPropertiesToDataSet()](#void-dumpmodelpropertiestodataset) | Derived class implements method to Dump Model properties into the DataSet
| [GetFirstSubfileRow](#string-getfirstsubfilerowstring-recordhtml)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | For multiple-row subfile records, gets a string that contains only the fields that will show in the top row, dropping the rest
| [GetSessionTransactionID()](#string-getsessiontransactionid) | Gets a string value that represents the Transaction ID from the Session storage.
| [GetSubfileRecord](#string-getsubfilerecordstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a cached (in the Session storage) record data for a particular record format, identified by RRN 
| [LoadFeedbackValues()](#bool-loadfeedbackvalues) | Derived class implements method to load the Displayfile Feedback Area values.
| [LoadModelPropertiesFromDataSet](#void-loadmodelpropertiesfromdatasetbool-onlynonpostedfields)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Derived class implements method to load properties from the DataSet, and which properties
| [MyAjaxActionResult()](#jsonresult-myajaxactionresult) | Gets the JsonResult with a un-successful response code
| [MyAjaxActionResult](#jsonresult-myajaxactionresultredirectedexception-redirect)([RedirectedException](/reference/expo/qsys-expo-model/redirected-exception.html)) | Gets the JsonResult with a un-successful response code (redirect parameter ignored)
| [OnCopyBrowserToDspFile()](#void-oncopybrowsertodspfile) | Callback method right before the data submitted from the Client (browser) is copied to the workstation data on the Web Server.
| [OnCopyDspFileToBrowser()](#void-oncopydspfiletobrowser) | Callback method right before the workstation data is sent from the Web Server to the Client (browser)
| [OnGet()](#iactionresult-onget) | Gets the User's Page's request response
| [OnGetFake()](#iactionresult-ongetfake) | Gets the Fake (prototyping) Page request's response
| [OnJobEnding()](#void-onjobending) | Callback method notifying the server that a Job is ending
| [OnPost()](#iactionresult-onpost) | Gets the Post Request's Response
| [OnPostFake()](#iactionresult-onpostfake) | Gets the Fake (prototyping) Post Request's Response
| [SelectMyAction](#iactionresult-selectmyactionbool-valid)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Gets the IActionResult as a Page render
| [SetResponseIndicators()](#void-setresponseindicators) | Derived class implements method to set the Response Indicators
| [SetSubfileRecord](#void-setsubfilerecordstring-formatname-int-rrn-string-recordhtml)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the HTML for a record that needs to be cached in the Session Storage
| [StoreHostFilePath](#string-storehostfilepathstring-hostfilepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the full path for a particular host file in the Session Storage

### JsonResult AjaxGetIconCollectionActionResult()

Gets the JsonResult for a "getIconCollection" AJAX request

```cs
JsonResult AjaxGetIconCollectionActionResult()
```

### JsonResult AjaxGetRecordsActionResult()

Gets the JsonResult for a "getRecords" AJAX request

```cs
JsonResult AjaxGetRecordsActionResult()
```

### void ClearModelProperties()

Derived class implements method to Clear all model properties

```cs
void ClearModelProperties()
```

### void ClearSubfilesInSession()

Clears cached Session storage entries related to All Subfiles.

```cs
void ClearSubfilesInSession()
```

### void CommitJobSession()

Store the job session in the data store. 

```cs
void CommitJobSession()
```

### void DumpModelPropertiesToDataSet()

Derived class implements method to Dump Model properties into the DataSet

```cs
void DumpModelPropertiesToDataSet()
```

### string GetFirstSubfileRow([string recordHTML](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

For multiple-row subfile records, gets a string that contains only the fields that will show in the top row, dropping the rest

```cs
string GetFirstSubfileRow(string recordHTML)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordHTML | full record in HTML

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the HTML with only fields showing in the first row

### string GetSessionTransactionID()

Gets a string value that represents the Transaction ID from the Session storage.

```cs
string GetSessionTransactionID()
```

### string GetSubfileRecord([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a cached (in the Session storage) record data for a particular record format, identified by RRN 

```cs
string GetSubfileRecord(string formatName, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | record format name
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | relative record number

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the HTML text for the subfile record cached

### bool LoadFeedbackValues()

Derived class implements method to load the Displayfile Feedback Area values.

```cs
bool LoadFeedbackValues()
```

### void LoadModelPropertiesFromDataSet([bool onlyNonPostedFields](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Derived class implements method to load properties from the DataSet, and which properties

```cs
void LoadModelPropertiesFromDataSet(bool onlyNonPostedFields)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | onlyNonPostedFields | true if only the non-posted properties are loaded. Defaults to false

### JsonResult MyAjaxActionResult()

Gets the JsonResult with a un-successful response code

```cs
JsonResult MyAjaxActionResult()
```

### JsonResult MyAjaxActionResult([RedirectedException redirect](/reference/expo/qsys-expo-model/redirected-exception.html))

Gets the JsonResult with a un-successful response code (redirect parameter ignored)

```cs
JsonResult MyAjaxActionResult(RedirectedException redirect)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [RedirectedException](/reference/expo/qsys-expo-model/redirected-exception.html) | redirect | Redirected Exception

#### Returns

| Type | Description
| --- | ---
| [JsonResult](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.jsonresult?view=aspnetcore-8.0) | the JsonResult

### void OnCopyBrowserToDspFile()

Callback method right before the data submitted from the Client (browser) is copied to the workstation data on the Web Server.

```cs
void OnCopyBrowserToDspFile()
```

### void OnCopyDspFileToBrowser()

Callback method right before the workstation data is sent from the Web Server to the Client (browser)

```cs
void OnCopyDspFileToBrowser()
```

### IActionResult OnGet()

Gets the User's Page's request response

```cs
IActionResult OnGet()
```

### IActionResult OnGetFake()

Gets the Fake (prototyping) Page request's response

```cs
IActionResult OnGetFake()
```

### void OnJobEnding()

Callback method notifying the server that a Job is ending

```cs
void OnJobEnding()
```

### IActionResult OnPost()

Gets the Post Request's Response

```cs
IActionResult OnPost()
```

### IActionResult OnPostFake()

Gets the Fake (prototyping) Post Request's Response

```cs
IActionResult OnPostFake()
```

### IActionResult SelectMyAction([bool valid](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Gets the IActionResult as a Page render

```cs
IActionResult SelectMyAction(bool valid)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | valid | Ignored

#### Returns

| Type | Description
| --- | ---
| [IActionResult](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.iactionresult?view=aspnetcore-8.0) | the Action result

### void SetResponseIndicators()

Derived class implements method to set the Response Indicators

```cs
void SetResponseIndicators()
```

### void SetSubfileRecord([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string recordHtml](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the HTML for a record that needs to be cached in the Session Storage

```cs
void SetSubfileRecord(string formatName, int rrn, string recordHtml)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | record format name
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | relative record number
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordHtml | HTML text

### string StoreHostFilePath([string hostFilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the full path for a particular host file in the Session Storage

```cs
string StoreHostFilePath(string hostFilePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | hostFilePath | The host file full path.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The ID for the stored host file.
