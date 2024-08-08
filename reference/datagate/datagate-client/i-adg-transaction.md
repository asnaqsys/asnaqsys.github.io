---
title: "IAdgTransaction interface     | QSYS API Reference Guide"
description: "Defines the contract for a transaction in the ASNA DataGate client. "
last_modified_at: 2024-08-08T21:41:32Z
---

Defines the contract for a transaction in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>
## Thread Safety

Instance members of this type are not guaranteed to be thread safe.


## Remarks
This interface is used to manage transactions in the ASNA DataGate client. 
It provides methods for committing and rolling back transactions, 
and properties to get the connection and transaction level details.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets the connection associated with the transaction. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Name | Gets the name of the transaction. |
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | TransactionLevel | Gets the transaction level for the current transaction. |

## Methods

| Signature | Description |
| --- | --- |
| [Commit()](#void-commit) | Commits the current transaction.
| [Commit](#void-commitstring-transactionname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Commits the current transaction with a specified transaction name.
| [Rollback()](#void-rollback) | Rolls back the current transaction.

### void Commit()

Commits the current transaction.

```cs
void Commit()
```

### void Commit([string TransactionName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Commits the current transaction with a specified transaction name.

```cs
void Commit(string TransactionName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | TransactionName | The name of the transaction to commit.

### void Rollback()

Rolls back the current transaction.

```cs
void Rollback()
```
