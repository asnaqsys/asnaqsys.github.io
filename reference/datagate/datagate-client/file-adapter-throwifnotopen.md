---
title: "FileAdapter.ThrowIfNotOpen Method"
description: "Checks if the provided reference is not null. If null, throws a dgException"
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Checks if the provided reference is not null. If it is not null, the refernce is returned. If it is null, a [dgException](/reference/datagate/datagate-common/dg-exception.html) is thrown with its `Error` property set to [dgErrorNumber.dgEaNOFILE](/reference/datagate/datagate-common/dg-error-number.html).

```cs
static T ThrowIfNotOpen<T>(T? object)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type) | object | The state to check. |

#### Returns

| Type | Description |
| --- | --- |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type) | The object if it is not null. |


## See Also
- [FileAdapter class](file-adapter.html)
