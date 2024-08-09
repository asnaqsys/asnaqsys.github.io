---
title: "DataGateCredentialExtensions class"
description: "Provides extension methods for the IDataGateCredential interface. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides extension methods for the IDataGateCredential interface.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [IsStarDomainCredential](#bool-isstardomaincredentialidatagatecredential-dgc)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html)) | Determines whether the specified IDataGateCredential is a StarDomain credential.
| [ThrowIfNotUserPassword](#void-throwifnotuserpasswordidatagatecredential-dgc-userpasswordcredential-upc)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html), [UserPasswordCredential&](/reference/datagate/datagate-providers/user-password-credential.html)) | Throws an exception if the specified IDataGateCredential is not a UserPassword credential.

### bool IsStarDomainCredential([IDataGateCredential dgc](/reference/datagate/datagate-providers/i-datagate-credential.html))

Determines whether the specified IDataGateCredential is a StarDomain credential.

```cs
bool IsStarDomainCredential(IDataGateCredential dgc)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | dgc | The IDataGateCredential to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the specified IDataGateCredential is a StarDomain credential; otherwise, false.

### void ThrowIfNotUserPassword([IDataGateCredential dgc](/reference/datagate/datagate-providers/i-datagate-credential.html), [UserPasswordCredential& upc](/reference/datagate/datagate-providers/user-password-credential.html))

Throws an exception if the specified IDataGateCredential is not a UserPassword credential.

```cs
void ThrowIfNotUserPassword(IDataGateCredential dgc, UserPasswordCredential& upc)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | dgc | The IDataGateCredential to check.
| [UserPasswordCredential&](/reference/datagate/datagate-providers/user-password-credential.html) | upc | The UserPasswordCredential to check.
