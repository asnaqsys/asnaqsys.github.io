---
title: "UserPasswordCredential class"
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
| [UserPasswordCredential](user-password-credential-ctor.html#userpasswordcredential-string-string-passwordtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [PasswordType](/reference/datagate/datagate-common/password-type.html)) | Construct a UserPasswordCredential instance from component parts.
| [UserPasswordCredential()](user-password-credential-ctor.html#userpasswordcredential) | Construct a UserPasswordCredential with default values.

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
| [Clone()](user-password-credential-clone.html#object-clone) | Creates a new object that is a copy of the current instance.
| [Equals](user-password-credential-equals.html#bool-equals-idatagatecredential-other)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html)) | Determines whether the current instance of  is equal to the specified instance.
| [GetHashCodeInternal()](user-password-credential-gethashcodeinternal.html#int-gethashcodeinternal) | Serves as the default hash function for the current instance.

