---
title: IAdgTransaction Interface

---

**IAdgTransaction** models database transaction management objects for database providers that support transaction processing. Instances of **IAdgTransaction** are manufactured by the [AdgConnection.BeginTransaction](adg-connection-class-begin-transaction-method-main.html) and [AdgConnection.BeginAutoTransaction](adg-connection-class-begin-auto-transaction-method-main.html) methods.

For a list of all members of this type, see [IAdgTransaction Members](iadg-transaction-members.html).

[ASNA.DataGate.Client](datagate-client-namespace.html) <br /> **ASNA.DataGate.Client.<span>IAdgTransaction</span>** 
<pre class="prettyprint">&lt;Serializable&gt; **Public Class IAdgTransaction** </pre>

## Thread Safety

Instance members of this type are not guaranteed to be thread safe.
## Remarks

**IAdgTransaction** provides properties and methods for managing database transaction processing. An instance of **IAdgTransaction** is associated with a single database connection (as referenced by the [ Connection](iadg-transaction-class-connection-property.html) property), which defines the operational context of a transaction. A [TransactionLevel](iadg-transaction-class-transaction-level-property.html) is assigned that the database provider may use to prioritize a transaction. The transaction is given an application-specific identifier ([Name](iadg-transaction-class-name-property.html) ) that the database provider may use to identify transaction resources. 

Methods are provided to accept and cancel database modifications occuring within the boundaries of the transaction ([Commit](iadg-transaction-class-commit-methods.html) and [Rollback](iadg-transaction-class-rollback-method.html) respectively). 

DG provides two types of transaction objects - automatic and manual transactions, both of which implement **IAdgTransaction** . 

Manual transactions objects are constructed by the **AdgConnection.BeginTransaction** method. The database provider begins a transaction context upon successful construction of the manual transaction object. The behavior of the manual transaction with regard to the **Commit** and **Rollback** methods is database provider platform-dependent. Some providers may end the transaction context after a call to **Commit** or **Rollback** , while others may continue the transaction context after these method calls.

Automatic transactions are constructed by the **AdgConnection.BeginAutoTransaction** method. A transaction context is begun by the database provider upon successful construction of the automatic transaction object. The **Commit** and **Rollback** methods of an automatic transaction object perform the same functions as those of a manual transaction object. However, after successfully accepting or cancelling database modifications, both methods of an automatic transaction end the current transaction context and begin a new transaction using the parameters of the preceding transaction. The **IAdgTransaction** instance assumes control of the new transaction context. An automatic transaction is intended to emulate the behavior of IBM i database transactions for all database platforms.

With some database providers, calling the **Dispose** method to end the transaction context is critical to proper transaction processing. With both types of transaction objects, it is recommended that applications explicitly call **Dispose** to end the current transaction context rather than relying on the behavior of a specific database provider in ending the transaction.

Nested database transaction are allowed with transaction processing but this requires you to control the transaction flow from object to object while maintaining the security, recovery, concurrency, and integrity within the transaction boundary. DG does not restrict nested transactions but the database provider may have mechanisms that prevent or limit such usage. Please consult the database provider's documentation for details.

At the time of this writing, only the IBM i database provider supports transaction processing.
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IAdgTransaction Members](iadg-transaction-members.html)
      <br />
[AdgConnection Class](adg-connection-class.html)
      <br />
      [BeginTransaction 
					Method](adg-connection-class-begin-transaction-method-main.html)
      <br />
      [BeginAutoTransaction 
					Method](adg-connection-class-begin-auto-transaction-method-main.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

