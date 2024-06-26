---
title: IDSDataArea interface
description: "Describes a data structure that can be stored in a data area. "
last_modified_at: 2024-06-26T20:27:05Z
---

Describes a data structure that can be stored in a data area.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [In](#void-inidataarea-dataarea)([IDataArea](/reference/datagate/datagate-client/i-data-area.html)) | Gets a data area and copies its contents into the data structure.
| [Out](#void-outidataarea-dataarea)([IDataArea](/reference/datagate/datagate-client/i-data-area.html)) | Copies the data structure into the given data area.

### void In([IDataArea dataArea](/reference/datagate/datagate-client/i-data-area.html))

Gets a data area and copies its contents into the data structure.

```cs
void In(IDataArea dataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | dataArea | The data area to use.

### void Out([IDataArea dataArea](/reference/datagate/datagate-client/i-data-area.html))

Copies the data structure into the given data area.

```cs
void Out(IDataArea dataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | dataArea | The data area to use.
