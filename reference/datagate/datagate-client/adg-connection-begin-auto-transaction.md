---
title: "AdgConnection.BeginAutoTransaction Method"
description: "Begins a transaction that is automatically committed or rolled back by the system."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

Begins a transaction that is automatically committed or rolled back by the system.

## Overloads

| Signature | Description |
| --- | --- |
| [BeginAutoTransaction](#iadgtransaction-beginautotransactiontransactionlevel-tl-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level and options.
| [BeginAutoTransaction](#iadgtransaction-beginautotransactionstring-name-string-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified name and options.
| [BeginAutoTransaction](#iadgtransaction-beginautotransactiontransactionlevel-tl-string-name-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level, name, and options.

## IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified transaction level and options.


#### Remarks
This method begins a new automatic transaction with the specified transaction level and options. An automatic transaction is a transaction that is automatically committed or rolled back by the system. The transaction level determines the isolation level of the transaction. The options parameter can be used to specify additional options for the transaction. This method calls the BeginAutoTransaction method with an empty string for the name parameter, meaning the transaction will not have a name.

This method begins an _automatic transaction_ for those database providers that support transaction processing. The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`. This version of **BeginAutoTransaction** produces an anonymous transaction, where the `Name` property of the returned **IAdgTransaction** object is the empty string.
 
An automatic transaction (as initiated by **BeginAutoTransaction**) is distinguished from a manual transaction (as initiated by the `BeginTransaction` methods) by the behaviors of the `IAdgTransaction.Commit Method` and `IAdgTransaction.Rollback` methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**. Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Automatic transactions can be used when an application expects the behavior of **IAdgTransaction** to be uniform regardless of the transaction-enabled database provider in use. However, note that at the time of this writing, only the IBM i database provider is transaction-enabled. For future multi-platform compatibility, use of automatic transactions is recommended. For the finest level of control over each transaction, use of manual transactions is recommended (see **BeginTransaction**).
 
_tl_ specifies the initial transaction level and is used to initialize the value of the `TransactionLevel` property of the **IAdgTransaction** object returned.
 
_Options_ specifies command options for initiating the new **IAdgTransaction** object specific to the database provider. For example, transactions on IBM i database providers are initiated via the "STRCMTCTL" CL command, with the "LCKLVL", "TEXT", and "CMTSCOPE(*JOB)" parameters. Other parameters not specified by DataGate, such as "NFYOBJ" and "DFTJRN", may be specified via _Options_ (e.g. "NFYOBJ(MYLIB/MYOBJ *MSGQ) DFTJRN(MYLIB/MYJRN)" ). If other command options are not required, specify the empty string or null reference for _Options_. Note that non-empty string values for _Options_ may defeat the multi-platform compatibility provided by automatic transactions. In an automatic transaction, the value of _Options_ is used for each new transaction created by **Commit** and **Rollback**.

```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.


## IAdgTransaction BeginAutoTransaction([string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified name and options.


#### Remarks
This method begins a new automatic transaction with the specified name and options. An automatic transaction is a transaction that is automatically committed or rolled back by the system. The transaction level for this method is set to Medium by default. The name parameter can be used to specify a name for the transaction. The options parameter can be used to specify additional options for the transaction.

This method begins an _automatic transaction_ for those database providers that support transaction processing. The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`. This version of **BeginAutoTransaction** produces a transaction where the `TransactionLevel` property of the returned **IAdgTransaction** object has the value `TransactionLevel.Medium`.
 
An automatic transaction (as initiated by **BeginAutoTransaction**) is distinguished from a manual transaction (as initiated by the `BeginTransaction` methods) by the behaviors of the `IAdgTransaction.Commit` method and `IAdgTransaction.Rollback` methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**. Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Automatic transactions can be used when an application expects the behavior of **IAdgTransaction** to be uniform regardless of the transaction-enabled database provider in use. However, note that at the time of this writing, only the IBM i database provider is transaction-enabled. For future multi-platform compatibility, use of automatic transactions is recommended. For the finest level of control over each transaction, use of manual transactions is recommended (see **BeginTransaction**).
 
_Name_ may be used by the database provider to identify transaction resources. _Name_ initializes the `Name` property of the **IAdgTransaction** object returned. Specifying the empty string or a null reference for _Name_ results in an anonymous transaction.
 
_Options_ specifies command options for initiating the new **IAdgTransaction** object specific to the database provider. For example, transactions on IBM i database providers are initiated via the "STRCMTCTL" CL command, with the "LCKLVL", "TEXT", and "CMTSCOPE(*JOB)" parameters. Other parameters not specified by DCS, such as "NFYOBJ" and "DFTJRN", may be specified via _Options_ (e.g. "NFYOBJ(MYLIB/MYOBJ *MSGQ) DFTJRN(MYLIB/MYJRN)" ). If other command options are not required, specify the empty string or null reference for _Options_. Note that non-empty string values for _Options_ may defeat the multi-platform compatibility provided by automatic transactions. In an automatic transaction, the value of _Options_ is used for each new transaction created by **Commit** and **Rollback**.


```cs
IAdgTransaction BeginAutoTransaction(string Name, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

## IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified transaction level, name, and options.


#### Remarks
This method begins a new automatic transaction with the specified transaction level, name, and options.An automatic transaction is a transaction that is automatically committed or rolled back by the system. The transaction level determines the isolation level of the transaction.The name parameter can be used to specify a name for the transaction. The options parameter can be used to specify additional options for the transaction. The transaction attributes are set to CommitAndRestart and RollbackAndRestart, meaning that if the transaction is committed or rolled back, it will automatically restart.

This method begins an _automatic transaction_ for those database providers that support transaction processing.  The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`.
 
An automatic transaction (as initiated by **BeginAutoTransaction**) is distinguished from a manual transaction (as initiated by the `BeginTransaction` methods) by the behaviors of the `IAdgTransaction.Commit` method and `IAdgTransaction.Rollback` methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**. Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Automatic transactions can be used when an application expects the behavior of **IAdgTransaction** to be uniform regardless of the transaction-enabled database provider in use. However, note that at the time of this writing, only the IBM i database provider is transaction-enabled. For future multi-platform compatibility, use of automatic transactions is recommended. For the finest level of control over each transaction, use of manual transactions is recommended (see **BeginTransaction**).
 
_Name_ may be used by the database provider to identify transaction resources. _Name_ initializes the `Name` property of the **IAdgTransaction** object returned. Specifying the empty string or a null reference for _Name_ results in an anonymous transaction.
 
_tl_ specifies the initial transaction level.  _tl_ is used to initialize the value of the `TransactionLevel` property of the **IAdgTransaction** object returned.
 
_Options_ specifies command options for initiating the new **IAdgTransaction** object specific to the database provider. For example, transactions on IBM i database providers are initiated via the "STRCMTCTL" CL command, with the "LCKLVL", "TEXT", and "CMTSCOPE(*JOB)" parameters. Other parameters not specified by DCS, such as "NFYOBJ" and "DFTJRN", may be specified via _Options_ (e.g. "NFYOBJ(MYLIB/MYOBJ *MSGQ) DFTJRN(MYLIB/MYJRN)" ). If other command options are not required, specify the empty string or null reference for _Options_. Note that non-empty string values for _Options_ may defeat the multi-platform compatibility provided by automatic transactions. In an automatic transaction, the value of _Options_ is used for each new transaction created by **Commit** and **Rollback**.


```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Name, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.
