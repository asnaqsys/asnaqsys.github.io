---
title: "AuthorityEntry class          | QSYS API Reference Guide"
description: "The AuthorityEntry class describes a user or group authorization to a database object. "
last_modified_at: 2024-08-09T16:18:40Z
---

The AuthorityEntry class describes a user or group authorization to a database object.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [AuthorityEntry()](#authorityentry) | Initializes a new instance of the  class with default values.
| [AuthorityEntry](#authorityentrystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified user-name and default values for other properties.
| [AuthorityEntry](#authorityentrystring-authoritytypes)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html)) | Initializes a new instance of the  class with the specified user-name and authority type, and sets the IsGroupAccount property to false.
| [AuthorityEntry](#authorityentrystring-authoritytypes-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the  class with the specified user-name, authority type, and group account status.

### AuthorityEntry()

Initializes a new instance of the  class with default values.

```cs
AuthorityEntry()
```

### AuthorityEntry([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified user-name and default values for other properties.

```cs
AuthorityEntry(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | username | The user-name for the authority entry.

### AuthorityEntry([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html))

Initializes a new instance of the  class with the specified user-name and authority type, and sets the IsGroupAccount property to false.

```cs
AuthorityEntry(String, AuthorityTypes)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | username | The user-name for the authority entry.
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | authorityType | The type of authority for the entry.

### AuthorityEntry([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the  class with the specified user-name, authority type, and group account status.

```cs
AuthorityEntry(String, AuthorityTypes, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | username | The user-name for the authority entry.
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | authorityType | The type of authority for the entry.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isGroupAccount | A boolean value indicating whether the authority entry is for a group account.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | AuthorityType | Gets or sets the type of authority for the authority entry. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsGroupAccount | Gets or sets a value indicating whether the authority entry is for a group account. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Username | Gets or sets the user-name for the authority entry. |
