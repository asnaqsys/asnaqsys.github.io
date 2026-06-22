---
title: "DataGateCredentialExtensions.ThrowIfNotUserPassword Method"
description: "Throws an exception if the specified IDataGateCredential is not a UserPassword credential."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Throws an exception if the specified IDataGateCredential is not a UserPassword credential.

<a id="void-throwifnotuserpassword-idatagatecredential-dgc-userpasswordcredential-upc"></a>
## void ThrowIfNotUserPassword(IDataGateCredential dgc, UserPasswordCredential& upc)

Throws an exception if the specified IDataGateCredential is not a UserPassword credential.

```cs
void ThrowIfNotUserPassword(IDataGateCredential dgc, UserPasswordCredential& upc)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | dgc | The IDataGateCredential to check.
| [UserPasswordCredential&](/reference/datagate/datagate-providers/user-password-credential.html) | upc | The UserPasswordCredential to check.

## See Also
- [DataGateCredentialExtensions class](datagate-credential-extensions.html)
