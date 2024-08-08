---
title: "SessionStorage class          | QSYS API Reference Guide"
description: "Defines the SessionStorage class "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines the SessionStorage class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

The `SessionStorage` is a class that is used to provide `state` to a [stateless environment](https://en.wikipedia.org/wiki/Stateless_protocol) such as the Internet Web.

IBM i Applications were designed with the [Traditional Three-Tier client-server Application Architecture](https://www.ibm.com/cloud/learn/three-tier-architecture). This architecture is stateful.

The `SessionStorage` is the class that provides the runtime functionality to bridge the traditional Application architecture into the modern Web model. 
## Constructors

| Name | Description |
| --- | --- |
| [SessionStorage](#sessionstorageisession)([ISession](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.isession)) | Initializes a new instance of SessionStorage class

### SessionStorage([ISession](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.isession))

Initializes a new instance of SessionStorage class

```cs
SessionStorage(ISession)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ISession](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.isession) | Session | A reference to the session.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AreaList | Gets or sets the names of the Areas from/to the Session |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MessageFilesFolder | Gets or sets the name of the MessageFiles folder from/to the Session |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MonaLisaHost | Gets or sets the Monalisa Host Name from/to the Session |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MonaLisaPort | Gets or sets the Monalisa IP Port number from/to the Session |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SingleFakeSession | Gets or sets the Single JobSession for running in Fake Mode |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SingleJobNumber | Gets or sets the job number for sites running in Single Job configuration. |

## Methods

| Signature | Description |
| --- | --- |
| [GetSessionString](#string-getsessionstringstring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string from a key on the Session
| [SetSessionString](#void-setsessionstringstring-key-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets a string value to a key in the Session

### string GetSessionString([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a string from a key on the Session

```cs
string GetSessionString(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | session key

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | stored string value

### void SetSessionString([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets a string value to a key in the Session

```cs
void SetSessionString(string key, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | session key
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | string value
