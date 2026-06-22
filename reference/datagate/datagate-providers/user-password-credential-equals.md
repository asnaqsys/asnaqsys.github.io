---
title: "UserPasswordCredential.Equals Method"
description: "Determines whether the current instance of is equal to the specified instance."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the current instance of is equal to the specified instance.

<a id="bool-equals-idatagatecredential-other"></a>
## bool Equals(IDataGateCredential other)

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

## See Also
- [UserPasswordCredential class](user-password-credential.html)
