---
title: "DataGateCredential class      | QSYS API Reference Guide"
description: "Provides a base class for DataGate credentials. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides a base class for DataGate credentials.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DataGateCredential](#datagatecredentialcredentialtype)([CredentialType](/reference/datagate/datagate-providers/credential-type.html)) | Initializes a new instance of the DataGateCredential class with the specified CredentialType.

### DataGateCredential([CredentialType](/reference/datagate/datagate-providers/credential-type.html))

Initializes a new instance of the DataGateCredential class with the specified CredentialType.

```cs
DataGateCredential(CredentialType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CredentialType](/reference/datagate/datagate-providers/credential-type.html) | type | The type of credentials used for authentication.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [CredentialType](/reference/datagate/datagate-providers/credential-type.html) | CredentialType | Gets the type of credentials used for authentication. |

## Methods

| Signature | Description |
| --- | --- |
| [Clone()](#object-clone) | Creates a new object that is a copy of the current instance.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.
| [Equals](#bool-equalsidatagatecredential-other)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html)) | Determines whether the specified IDataGateCredential is equal to the current object.
| [GetHashCode()](#int-gethashcode) | Returns a hash code for the current object.
| [GetHashCodeInternal()](#int-gethashcodeinternal) | When overridden in a derived class, returns a hash code for the current object.

### object Clone()

Creates a new object that is a copy of the current instance.

```cs
object Clone()
```

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the specified object is equal to the current object.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current object.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the specified object is equal to the current object; otherwise, false.

### bool Equals([IDataGateCredential other](/reference/datagate/datagate-providers/i-datagate-credential.html))

Determines whether the specified IDataGateCredential is equal to the current object.

```cs
bool Equals(IDataGateCredential other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | other | The IDataGateCredential to compare with the current object.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the specified IDataGateCredential is equal to the current object; otherwise, false.

### int GetHashCode()

Returns a hash code for the current object.

```cs
int GetHashCode()
```

### int GetHashCodeInternal()

When overridden in a derived class, returns a hash code for the current object.

```cs
int GetHashCodeInternal()
```
