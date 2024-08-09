---
title: "UserPasswordCredential class  | QSYS API Reference Guide"
description: "The user name and password information of UserPasswordCredential may be used to establish authenticated connections to databases that require such inf"
last_modified_at: 2024-08-09T17:25:07Z
---

The user name and password information of UserPasswordCredential may be
used to establish authenticated connections to databases that require
such information.

User and Password properties may be set or initialized to null values,
in which case the return values are empty values.  These properties
never return null values.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [DataGateCredential](/reference/datagate/datagate-providers/datagate-credential.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [UserPasswordCredential](#userpasswordcredentialstring-string-passwordtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [PasswordType](/reference/datagate/datagate-common/password-type.html)) | Construct a UserPasswordCredential instance from component parts.
| [UserPasswordCredential()](#userpasswordcredential) | Construct a UserPasswordCredential with default values.

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

### UserPasswordCredential()

Construct a UserPasswordCredential with default values.

```cs
UserPasswordCredential()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Password | Password information as a clear-text value. |
| [PasswordType](/reference/datagate/datagate-common/password-type.html) | PasswordType | Password handling information. |
| [UserPasswordCredential](/reference/datagate/datagate-providers/user-password-credential.html) | StarDomain | Gets the special UserPasswordCredential instance representing a domain user. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | User | Gets or sets a user name associated with the logon credential. |

## Methods

| Signature | Description |
| --- | --- |
| [Clone()](#object-clone) | Creates a new object that is a copy of the current instance.
| [Equals](#bool-equalsidatagatecredential-other)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html)) | Determines whether the current instance of  is equal to the specified instance.
| [GetHashCodeInternal()](#int-gethashcodeinternal) | Serves as the default hash function for the current instance.

### object Clone()

Creates a new object that is a copy of the current instance.


#### Remarks
This method is used to create a copy of the current instance of the UserPasswordCredential class. The copy is made by creating a new instance of the UserPasswordCredential class with the same user, password, and password type as the current instance.

```cs
object Clone()
```

### bool Equals([IDataGateCredential other](/reference/datagate/datagate-providers/i-datagate-credential.html))

Determines whether the current instance of  is equal to the specified instance.


#### Remarks
This method is used to compare the current instance with another instance of the UserPasswordCredential class. The comparison is based on the user, password type, and password of the instances.

```cs
bool Equals(IDataGateCredential other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | other | The instance to compare with the current instance.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the current instance is equal to the specified instance; otherwise, false.

### int GetHashCodeInternal()

Serves as the default hash function for the current instance.


#### Remarks
This method is used to generate a hash code for the current instance of the UserPasswordCredential class. It takes into account the user, password type, and password of the instance to generate a unique hash code.

```cs
int GetHashCodeInternal()
```
