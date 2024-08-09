---
title: "DataGateCredentialEqualityComparer class"
description: "Provides a comparer for IDataGateCredential objects, which supports equality comparisons. "
last_modified_at: 2024-08-09T16:18:40Z
---

Provides a comparer for IDataGateCredential objects, which supports equality comparisons.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DataGateCredentialEqualityComparer](/reference/datagate/datagate-providers/datagate-credential-equality-comparer.html) | Default | Gets the default instance of the DataGateCredentialEqualityComparer class. |

## Methods

| Signature | Description |
| --- | --- |
| [Equals](#bool-equalsidatagatecredential-x-idatagatecredential-y)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html), [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html)) | Determines whether the specified IDataGateCredential objects are equal.
| [GetHashCode](#int-gethashcodeidatagatecredential-obj)([IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html)) | Returns a hash code for the specified IDataGateCredential object.

### bool Equals([IDataGateCredential x](/reference/datagate/datagate-providers/i-datagate-credential.html), [IDataGateCredential y](/reference/datagate/datagate-providers/i-datagate-credential.html))

Determines whether the specified IDataGateCredential objects are equal.

```cs
bool Equals(IDataGateCredential x, IDataGateCredential y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | x | The first IDataGateCredential object to compare.
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | y | The second IDataGateCredential object to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the specified IDataGateCredential objects are equal; otherwise, false.

### int GetHashCode([IDataGateCredential obj](/reference/datagate/datagate-providers/i-datagate-credential.html))

Returns a hash code for the specified IDataGateCredential object.

```cs
int GetHashCode(IDataGateCredential obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | obj | The IDataGateCredential object for which a hash code is to be returned.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A hash code for the specified IDataGateCredential object.
