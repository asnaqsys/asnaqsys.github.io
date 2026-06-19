---
title: "IDataArea interface.Retrieve Method"
description: "Retrieves the value of the data area."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves the value of the data area.

## Overloads

| Signature | Description |
| --- | --- |
| [Retrieve](#object-retrieve)(object Retrieve()) | Retrieves the value of the data area. |
| [Retrieve](#string-retrieve-int-startingoffset-int-substringlength)(string Retrieve(int StartingOffset, int SubstringLength)) | Get a subset of the data in a character-type data area. |
| [Retrieve](#void-retrieve-progparm-value)(void Retrieve(ProgParm Value)) | Retrieves the value of the data area into a ProgParm value. |
| [Retrieve](#void-retrieve-progparm-value-int-startingoffset-int-substringlength)(void Retrieve(ProgParm Value, int StartingOffset, int SubstringLength)) | Retrieves a subset of the data area into a ProgParm value. |

<a id="object-retrieve"></a>
## object Retrieve()

Retrieves the value of the data area.

```cs
object Retrieve()
```

<a id="string-retrieve-int-startingoffset-int-substringlength"></a>
## string Retrieve(int StartingOffset, int SubstringLength)

Get a subset of the data in a character-type data area.

```cs
string Retrieve(int StartingOffset, int SubstringLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | StartingOffset | 0-based index of first character            of the subset.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | SubstringLength | The non-negative length of the            subset.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The specified subset as a string, or null if the dataarea is not a character type.

<a id="void-retrieve-progparm-value"></a>
## void Retrieve(ProgParm Value)

Retrieves the value of the data area into a ProgParm value.

```cs
void Retrieve(ProgParm Value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Value | The ProgParm value to retrieve into.

<a id="void-retrieve-progparm-value-int-startingoffset-int-substringlength"></a>
## void Retrieve(ProgParm Value, int StartingOffset, int SubstringLength)

Retrieves a subset of the data area into a ProgParm value.

```cs
void Retrieve(ProgParm Value, int StartingOffset, int SubstringLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Value | The ProgParm value to retrieve into.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | StartingOffset | The starting offset of the subset.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | SubstringLength | The length of the subset.

## See Also
- [IDataArea interface class](i-data-area.html)
