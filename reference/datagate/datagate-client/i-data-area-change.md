---
title: "IDataArea interface.Change Method"
description: "Changes the value of the data area to a boolean value."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Changes the value of the data area to a boolean value.

## Overloads

| Signature | Description |
| --- | --- |
| [Change](#void-change-bool-value)(void Change(bool Value)) | Changes the value of the data area to a boolean value. |
| [Change](#void-change-decimal-value)(void Change(decimal Value)) | Changes the value of the data area to a decimal value. |
| [Change](#void-change-string-value)(void Change(string Value)) | Changes the value of the data area to a string value. |
| [Change](#void-change-string-value-int-startingoffset-int-substringlength)(void Change(string Value, int StartingOffset, int SubstringLength)) | Changes a subset of the data area to a string value. |
| [Change](#void-change-progparm-value)(void Change(ProgParm Value)) | Changes the value of the data area to a ProgParm value. |
| [Change](#void-change-progparm-value-int-startingoffset-int-substringlength)(void Change(ProgParm Value, int StartingOffset, int SubstringLength)) | Changes a subset of the data area to a ProgParm value. |

<a id="void-change-bool-value"></a>
## void Change(bool Value)

Changes the value of the data area to a boolean value.

```cs
void Change(bool Value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Value | The boolean value to set.

<a id="void-change-decimal-value"></a>
## void Change(decimal Value)

Changes the value of the data area to a decimal value.

```cs
void Change(decimal Value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | Value | The decimal value to set.

<a id="void-change-string-value"></a>
## void Change(string Value)

Changes the value of the data area to a string value.

```cs
void Change(string Value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Value | The string value to set.

<a id="void-change-string-value-int-startingoffset-int-substringlength"></a>
## void Change(string Value, int StartingOffset, int SubstringLength)

Changes a subset of the data area to a string value.

```cs
void Change(string Value, int StartingOffset, int SubstringLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Value | The string value to set.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | StartingOffset | The starting offset of the subset.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | SubstringLength | The length of the subset.

<a id="void-change-progparm-value"></a>
## void Change(ProgParm Value)

Changes the value of the data area to a ProgParm value.

```cs
void Change(ProgParm Value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Value | The ProgParm value to set.

<a id="void-change-progparm-value-int-startingoffset-int-substringlength"></a>
## void Change(ProgParm Value, int StartingOffset, int SubstringLength)

Changes a subset of the data area to a ProgParm value.

```cs
void Change(ProgParm Value, int StartingOffset, int SubstringLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Value | The ProgParm value to set.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | StartingOffset | The starting offset of the subset.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | SubstringLength | The length of the subset.

## See Also
- [IDataArea interface class](i-data-area.html)
