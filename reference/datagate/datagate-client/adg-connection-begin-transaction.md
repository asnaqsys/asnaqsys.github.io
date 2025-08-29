---
title: "AdgConnection.BeginTransaction Method"
description: "Begins a database transaction."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

Begins a manual database transaction creating an instance of an [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) object with combinations of transaction locking level, name, and command options parameters specified.

## Overloads

| Signature | Description |
| --- | --- |
| [BeginTransaction](#iadgtransaction-begintransactiontransactionlevel-tl)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html)) | Begins a transaction with the specified transaction level.
| [BeginTransaction](#iadgtransaction-begintransactionstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified name.
| [BeginTransaction](#iadgtransaction-begintransactiontransactionlevel-tl-string-name)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level and name.
| [BeginTransaction](#iadgtransaction-begintransactiontransactionlevel-tl-string-name-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level, name, and options.


### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html))

Begins a transaction with the specified transaction level.


#### Remarks

This method begins a _manual transaction_ for those database providers that support transaction processing. The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`. This version of **BeginTransaction** produces an anonymous transaction, where the `Name` property of the returned **IAdgTransaction** object is the empty string.
 
A manual transaction (as initiated by **BeginTransaction**) is distinguished from an automatic transaction (as initiated by the `BeginAutoTransaction` methods) by the behaviors of the `IAdgTransaction.Commit`  and `IAdgTransaction.Rollback` methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**. Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Manual transactions should be used when an application requires a high degree of control over the transaction. Manual transactions can only be initiated with the **BeginTransaction** method. Further, manual transactions are not automatically renewed by DCS in the **Commit** and **Rollback** methods, as automatic transactions are. When multi-platform compatibility is of greater concern, use of automatic transactions is recommended (see **BeginAutoTransaction**). For the finest level of control over each transaction, use of manual transactions is recommended.
 
_tl_ specifies the initial transaction level and is used to initialize the value of the `TransactionLevel` property of the **IAdgTransaction** object returned.


```cs
IAdgTransaction BeginTransaction(TransactionLevel tl)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.




### IAdgTransaction BeginTransaction([string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins a transaction with the specified name.


#### Remarks

This method begins a _manual transaction_ for those database providers that support transaction processing.  The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`.
 
A manual transaction (as initiated by **BeginTransaction**) is distinguished from an automatic transaction (as initiated by the `BeginAutoTransaction` methods) by the behaviors of the `IAdgTransaction.Commit` and `IAdgTransaction.Rollback` methods.  **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries.  In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**.  Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Manual transactions should be used when an application requires a high degree of control over the transaction.  Manual transactions can only be initiated with the **BeginTransaction** method.  Further, manual transactions are not automatically renewed by DCS in the **Commit** and **Rollback** methods, as automatic transactions are.  When multi-platform compatibility is of greater concern, use of automatic transactions is recommended (see **BeginAutoTransaction**).  For the finest level of control over each transaction, use of manual transactions is recommended.
 
_Name_ may be used by the database provider to identify transaction resources.  _Name_ initializes the `Name` property of the **IAdgTransaction** object returned.  Specifying the empty string or a null reference for _Name_ results in an anonymous transaction.
 
The value of the `TransactionLevel` property of the **IAdgTransaction **object returned is `TransactionLevel.Medium`.

```cs
IAdgTransaction BeginTransaction(string Name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.




### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins a transaction with the specified transaction level and name.


#### Remarks

This method begins a _manual transaction_ for those database providers that support transaction processing.  The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`.
 
A manual transaction (as initiated by **BeginTransaction**) is distinguished from an automatic transaction (as initiated by the `BeginAutoTransaction`methods) by the behaviors of the `IAdgTransaction.Commit`  and `IAdgTransaction.Rollback` methods. **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries. In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**. Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Manual transactions should be used when an application requires a high degree of control over the transaction.  Manual transactions can only be initiated with the **BeginTransaction** method. Further, manual transactions are not automatically renewed by DCS in the **Commit** and **Rollback** methods, as automatic transactions are. When multi-platform compatibility is of greater concern, use of automatic transactions is recommended (see **BeginAutoTransaction**). For the finest level of control over each transaction, use of manual transactions is recommended.
 
_Name_ may be used by the database provider to identify transaction resources. _Name_ initializes the `Name` property of the **IAdgTransaction** object returned. Specifying the empty string or a null reference for _Name_ results in an anonymous transaction.
 
_tl_ specifies the initial transaction level and is used to initialize the value of the `TransactionLevel` property of the **IAdgTransaction** object returned.

This method uses an empty string for the options parameter, meaning the transaction will not have any additional options.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl, string Name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.




### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins a transaction with the specified transaction level, name, and options.

#### Remarks

This method begins a _manual transaction_ for those database providers that support transaction processing.  The returned **IAdgTransaction** object representing the transaction is associated with the database connection of `AdgConnection`.
 
A manual transaction (as initiated by **BeginTransaction**) is distinguished from an automatic transaction (as initiated by the `BeginAutoTransaction` methods) by the behaviors of the `IAdgTransaction.Commit` and `IAdgTransaction.Rollback` methods.  **Commit** and **Rollback** result in the acceptance and cancellation, respectively, of accumulated database modifications within the current transaction's boundaries.  In an automatic transaction, these methods also result in the end of the current transaction followed by the immediate creation of a new transaction under the control of **IAdgTransaction**.  Thus, the behavior of an automatic transaction is similar to the behavior of an IBM i database transaction for all database provider platforms.
 
Manual transactions should be used when an application requires a high degree of control over the transaction.  Manual transactions can only be initiated with the **BeginTransaction** method.  Further, manual transactions are not automatically renewed by DCS in the **Commit** and **Rollback** methods, as automatic transactions are.  When multi-platform compatibility is of greater concern, use of automatic transactions is recommended (see **BeginAutoTransaction**).  For the finest level of control over each transaction, use of manual transactions is recommended.
 
_Name_ may be used by the database provider to identify transaction resources.  _Name_ initializes the `Name` property of the **IAdgTransaction** object returned.  Specifying the empty string or a null reference for _Name _results in an anonymous transaction.
 
_tl_ specifies the initial transaction level and is used to initialize the value of the `TransactionLevel` property of the **IAdgTransaction** object returned.
 
_Options_ specifies command options for initiating the new **IAdgTranaction** object specific to the database provider.  For example, transactions on IBM i database providers are initiated via the "STRCMTCTL" CL command, with the "LCKLVL", "TEXT", and "CMTSCOPE(*JOB)" parameters.  Other parameters not specified by DCS, such as "NFYOBJ" and "DFTJRN", may be specified via _Options_ (e.g. "NFYOBJ(MYLIB/MYOBJ *MSGQ) DFTJRN(MYLIB/MYJRN)" ).  If other command options are not required, specify the empty string or null reference for _Options_.  Note that non-empty string values for _Options_ may restrict use of the application to a particular database provider.


```cs
IAdgTransaction BeginTransaction(TransactionLevel tl, string Name, string Options)
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
