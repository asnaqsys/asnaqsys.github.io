---
title: "AdgDataSet.NewKeyTable Method"
description: "Creates a new AdgKeyTable for the DataTable associated with the specified format name or index."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new AdgKeyTable for the DataTable associated with the specified format.

## Overloads

| Signature | Description |
| --- | --- |
| [NewKeyTable](#adgkeytable-newkeytableint)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a new AdgKeyTable for the DataTable associated with the specified format index.
| [NewKeyTable](#adgkeytable-newkeytablestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new AdgKeyTable for the DataTable associated with the specified format name.

## AdgKeyTable NewKeyTable(Int32)

Creates a new AdgKeyTable for the DataTable associated with the specified format index.

```cs
AdgKeyTable NewKeyTable(int iFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iFormat | The format index of the DataTable. |

#### Returns

| Type | Description |
| --- | --- |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | A new AdgKeyTable for the DataTable associated with the specified format index. |

### Remarks
Retrieves the AdgTable for the index, creates a new AdgKeyTable, and sets its key row.

## AdgKeyTable NewKeyTable(String)

Creates a new AdgKeyTable for the DataTable associated with the specified format name.

```cs
AdgKeyTable NewKeyTable(string strFormat)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | strFormat | The format name of the DataTable. |

#### Returns

| Type | Description |
| --- | --- |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | A new AdgKeyTable for the DataTable associated with the specified format name. |

### Remarks
Resolves the format via GetFormatIndex and delegates to the integer overload.

## See Also
- [AdgDataSet class](adg-data-set.html)
