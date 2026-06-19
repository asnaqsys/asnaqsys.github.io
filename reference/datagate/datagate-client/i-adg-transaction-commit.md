---
title: "IAdgTransaction interface.Commit Method"
description: "Commits the current transaction."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Commits the current transaction.

## Overloads

| Signature | Description |
| --- | --- |
| [Commit](#void-commit)(void Commit()) | Commits the current transaction. |
| [Commit](#void-commit-string-transactionname)(void Commit(string TransactionName)) | Commits the current transaction with a specified transaction name. |

<a id="void-commit"></a>
## void Commit()

Commits the current transaction.

```cs
void Commit()
```

<a id="void-commit-string-transactionname"></a>
## void Commit(string TransactionName)

Commits the current transaction with a specified transaction name.

```cs
void Commit(string TransactionName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | TransactionName | The name of the transaction to commit.

## See Also
- [IAdgTransaction interface class](i-adg-transaction.html)
