---
title: "UserPasswordCredential Constructors"
description: "Construct a UserPasswordCredential instance from component parts."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Construct a UserPasswordCredential instance from component parts.

## Overloads

| Name | Description |
| --- | --- |
| [UserPasswordCredential](#userpasswordcredential-string-string-passwordtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [PasswordType](/reference/datagate/datagate-common/password-type.html)) | Construct a UserPasswordCredential instance from component parts. |
| [UserPasswordCredential](#userpasswordcredential)() | Construct a UserPasswordCredential with default values. |

<a id="userpasswordcredential-string-string-passwordtype"></a>
### UserPasswordCredential([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [PasswordType](/reference/datagate/datagate-common/password-type.html))

Construct a UserPasswordCredential instance from component parts.

```cs
UserPasswordCredential(String, String, PasswordType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | user | Traditional user name for logon.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | password | Traditional character passphrase for logon,            or .            
| [PasswordType](/reference/datagate/datagate-common/password-type.html) | passwordType | For old servers with limited password            length requirements, set this to .            In most cases use the default value.

<a id="userpasswordcredential"></a>
### UserPasswordCredential()

Construct a UserPasswordCredential with default values.

```cs
UserPasswordCredential()
```

## See Also
- [UserPasswordCredential class](user-password-credential.html)
