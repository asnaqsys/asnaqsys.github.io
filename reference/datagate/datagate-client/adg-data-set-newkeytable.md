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

`FileAdapter` provides methods for accessing a file by key value using `AdgKeyTable`. **AdgKeyTable** is a class for manipulating a DataTable which represents a DataGate file key.  **NewKeyTable** generates an instance of **AdgKeyTable** corresponding to a key in a particular file format.  Generally, this is the way application programs create key buffers for use in <b>FileAdapter</b> keyed access methods.

This overload of **NewKeyTable** specifies the format as an index, where zero indicates the first format.



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

`FileAdapter` provides methods for accessing a file by key value using `AdgKeyTable`. **AdgKeyTable** is a class for manipulating a DataTable which represents a DataGate file key.  **NewKeyTable** generates an instance of **AdgKeyTable** corresponding to a key in a particular file format.  Generally, this is the way application programs create key buffers for use in **FileAdapter** keyed access methods.

This overload of **NewKeyTable** specifies the format by its name.


## See Also
- [AdgDataSet class](adg-data-set.html)
