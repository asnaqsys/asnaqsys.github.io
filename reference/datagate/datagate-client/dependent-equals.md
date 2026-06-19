---
title: "Dependent.Equals Method"
description: "Determines whether the specified is equal to the current ."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the specified is equal to the current .

## Overloads

| Signature | Description |
| --- | --- |
| [Equals](#bool-equals-dependent-other)(bool Equals(Dependent other)) | Determines whether the specified is equal to the current . |
| [Equals](#bool-equals-object-obj)(bool Equals(object obj)) | Determines whether the specified object is equal to the current . |

<a id="bool-equals-dependent-other"></a>
## bool Equals(Dependent other)

Determines whether the specified  is equal to the current .

#### Remarks
This method checks if the provided  is not null and if its , , and  properties are equal to those of the current instance.The comparison of  is case-insensitive.

```cs
bool Equals(Dependent other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Dependent](/reference/datagate/datagate-client/dependent.html) | other | The  to compare with the current .

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified  is equal to the current ; otherwise, false.

<a id="bool-equals-object-obj"></a>
## bool Equals(object obj)

Determines whether the specified object is equal to the current .

#### Remarks
This method overrides the  method.It casts the provided object to a  and calls the  method to perform the comparison.If the cast is unsuccessful (i.e., if the object is not a ), the method returns false.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current .

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is a  and is equal to the current ; otherwise, false.

## See Also
- [Dependent class](dependent.html)
