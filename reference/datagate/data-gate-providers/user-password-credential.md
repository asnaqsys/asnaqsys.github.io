---
title: UserPasswordCredential class
---

The user name and password information of UserPasswordCredential may be
used to establish authenticated connections to databases that require
such information.

User and Password properties may be set or initialized to null values,
in which case the values saved are empty values.  Thus these properties
never return null values.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [DataGateCredential](/reference/data-gate-providers/data-gate-credential.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [UserPasswordCredential](#userpasswordcredential-string-string-passwordtype-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [PasswordType](https://learn.microsoft.com/en-us/dotnet/api/)) | Construct a UserPasswordCredential instance from component parts.Note that the disposable password parameter reference is deep-copied, so the caller should dispose it.
| [UserPasswordCredential()](#userpasswordcredential-) | Construct a UserPasswordCredential with default values.  The Userand Password properties are initialized to empty values.  You mustset these properties to valid values before using this to attemptto authenticate a database connection.

### UserPasswordCredential([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [PasswordType](https://learn.microsoft.com/en-us/dotnet/api/))

Construct a UserPasswordCredential instance from component parts.Note that the disposable password parameter reference is deep-copied, so the caller should dispose it.

```cs
UserPasswordCredential(String, String, PasswordType)
```

#### Parameters
| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | user | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | password | 
| [PasswordType](https://learn.microsoft.com/en-us/dotnet/api/) | passwordType | 

### UserPasswordCredential()

Construct a UserPasswordCredential with default values.  The Userand Password properties are initialized to empty values.  You mustset these properties to valid values before using this to attemptto authenticate a database connection.

```cs
UserPasswordCredential()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
|  | StarDomain | Gets a UserPasswordCredential instance representing a domain user. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | User | Gets or sets a user name associated with the logon credential.Note that setting this to the special value "*DOMAIN" has the sideeffect of erasing the Password property value. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Password | Password information as a clear-text value. |
| [PasswordType](https://learn.microsoft.com/en-us/dotnet/api/) | PasswordType | Gets or sets the type of the password associated with the UserPasswordCredential. |

## Methods

| Signature | Description |
| --- | --- |
| [Clone()](#clone-) | Creates a new object that is a copy of the current UserPasswordCredential instance.
| [Equals](#equals-idatagatecredential-)([IDataGateCredential](/reference/data-gate-providers/i-data-gate-credential.html)) | Determines whether the specified IDataGateCredential is equal to the current UserPasswordCredential.
| [GetHashCodeInternal()](#gethashcodeinternal-) | Serves as the default hash function.

### object Clone()

Creates a new object that is a copy of the current UserPasswordCredential instance.

```cs
object Clone()
```

### bool Equals([IDataGateCredential other](/reference/data-gate-providers/i-data-gate-credential.html))

Determines whether the specified IDataGateCredential is equal to the current UserPasswordCredential.

```cs
bool Equals(IDataGateCredential other)
```

#### Parameters
| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/data-gate-providers/i-data-gate-credential.html) | other | 

#### Returns
| Type | Description
| --- | ---
true if the specified IDataGateCredential is equal to the current UserPasswordCredential; otherwise, false.

| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified IDataGateCredential is equal to the current UserPasswordCredential; otherwise, false.

### int GetHashCodeInternal()

Serves as the default hash function.

```cs
int GetHashCodeInternal()
```