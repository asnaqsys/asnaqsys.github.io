---
title: IAdgTransaction.Rollback Method

---

Cancel changes to the database that have been performed within the current transaction context.

```cs
 public virtual void Rollback();
```


## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEccIORECERR | Recoverable I/O error occurred in commit/rollback operation. |
| dgEccIORECERR | Unrecoverable I/O error occurred in commit/rollback operation. |
| dgEUNKNOWN | An unknown error (unpublished by the data provider) occurred. |
| dgEsAS400ERROR | The database server encountered a system error. Details are available via the SystemError and Text fields of [dgException](dgexception-class.html). For IBM i database providers, further details are available in the job log corresponding to the database connection. |



## Remarks

**Rollback** is used to cancel any changes that have occurred, via [Connection](iadg-transaction-class-connection-property.html), within the current transaction. Database providers may implement other related platform-dependent side effects, such as repositioning file pointers and releasing record locks. Also, database providers may have restrictions on the number of times [ Commit](iadg-transaction-class-commit-methods.html) and/or **Rollback** may be invoked within a single transaction context. Please consult the database provider's documentation for details.

When invoked on the automatic transaction implementation of **IAdgTransaction** (see [AdgConnection.BeginAutoTransaction Method](adg-connection-class-begin-auto-transaction-method-main.html)), **Rollback** also ends the current transaction context and automatically begins a new transaction context using the parameters of the preceding transaction. The new transaction is under the control of **IAdgTransaction** .
## Requirements

<span> **Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span>
## See Also


[IAdgTransaction Class](iadg-transaction-class.html)
      <br />
[IAdgTransaction Class Members](iadg-transaction-members.html)
      <br />
[Commit Method](iadg-transaction-class-commit-methods.html)
      <br />
[AdgConnection Class](adg-connection-class.html)
      <br />
      [BeginAutoTransaction 
					Method](adg-connection-class-begin-auto-transaction-method-main.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

