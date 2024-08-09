---
title: "DSDataArea class              | QSYS API Reference Guide"
description: "Describes and manages the use of a Data Structure as a Data Area value. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes and manages the use of a Data Structure as a Data Area value.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [DSCallParm](/reference/runtime/qsys-runtime/ds-call-parm.html) | DSCallParm | A DSCallParm used in the In and Out Data Area operations. |

## Methods

| Signature | Description |
| --- | --- |
| [In](#void-inidataarea-idataarea)([IDataArea](/reference/datagate/datagate-client/i-data-area.html)) | Retrieves the Data Structure from the given Data Area.
| [Out](#void-outidataarea-idataarea)([IDataArea](/reference/datagate/datagate-client/i-data-area.html)) | Stores the Data Structure in the given Data Area.

### void In([IDataArea iDataArea](/reference/datagate/datagate-client/i-data-area.html))

Retrieves the Data Structure from the given Data Area.

```cs
void In(IDataArea iDataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | iDataArea | The Data Area to access.

### void Out([IDataArea iDataArea](/reference/datagate/datagate-client/i-data-area.html))

Stores the Data Structure in the given Data Area.

```cs
void Out(IDataArea iDataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | iDataArea | The Data Area to access.
