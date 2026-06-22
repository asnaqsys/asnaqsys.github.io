---
title: "DataGateCredential.Equals Method"
description: "Determines whether the specified object is equal to the current object."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the specified object is equal to the current object.

## Overloads

| Signature | Description |
| --- | --- |
| [Equals](#bool-equals-object-obj)(bool Equals(object obj)) | Determines whether the specified object is equal to the current object. |
| [Equals](#bool-equals-idatagatecredential-other)(bool Equals(IDataGateCredential other)) | Determines whether the specified IDataGateCredential is equal to the current object. |

<a id="bool-equals-object-obj"></a>
## bool Equals(object obj)

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

<a id="bool-equals-idatagatecredential-other"></a>
## bool Equals(IDataGateCredential other)

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

## See Also
- [DataGateCredential class](datagate-credential.html)
