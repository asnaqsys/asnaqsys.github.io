---
title: "HostResourceHandler class     | QSYS API Reference Guide"
description: "Facilities to deal with resources available in the Host server. "
last_modified_at: 2024-08-09T17:26:04Z
---

Facilities to deal with resources available in the Host server.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [GetContentType](#string-getcontenttypestring-filepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determine the MIME type associated with a file extension.
| [GetHostFile](#iactionresult-gethostfilehttpcontext-httpcontext-string-hostfileid)([HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get a file stored at the host.

### string GetContentType([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determine the MIME type associated with a file extension.

```cs
string GetContentType(string filePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | The file path with an extension.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The MIME type

### IActionResult GetHostFile([HttpContext httpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0), [string hostFileID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get a file stored at the host.

```cs
IActionResult GetHostFile(HttpContext httpContext, string hostFileID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [HttpContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.httpcontext?view=aspnetcore-8.0) | httpContext | The information associated with the current HTTP request.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | hostFileID | The identifier for the requested host file.

#### Returns

| Type | Description
| --- | ---
| [IActionResult](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.iactionresult?view=aspnetcore-8.0) | The file contents result or a bad request result.
