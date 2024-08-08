---
title: "RedirectedException class     | QSYS API Reference Guide"
description: "Represents an exception used to indicate a redirection action within the application. "
last_modified_at: 2024-08-08T21:42:10Z
---

Represents an exception used to indicate a redirection action within the application.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RedirectedException](#redirectedexceptionstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class.

### RedirectedException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class.

```cs
RedirectedException(String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newUrl | The new URL to which the request is redirected.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newArea | The new area to which the request is redirected. Optional.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets a message that describes the current exception, indicating the redirection target. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NewArea | Gets or sets the new area to which the request is redirected. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NewUrl | Gets or sets the new URL to which the request is redirected. |
