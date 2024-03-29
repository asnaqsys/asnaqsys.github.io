---
title: TransactionLevel Enumeration

---

The **TransactionLevel** enumerated constant defines values for the [ TransactionLevel](iadg-transaction-class-transaction-level-property.html) property of [IAdgTransaction](iadg-transaction-class.html).

```cs
 public enum TransactionLevel;
```


## Remarks

A parameter of type **TransactionLevel** may be specified by certain overloads of the [ AdgConnection.BeginAutoTransaction](adg-connection-class-begin-auto-transaction-method-main.html) and [ AdgConnection.BeginTransaction](adg-connection-class-begin-transaction-method-main.html) methods to create an instance of **IAdgTransaction** with the **TransactionLevel** property initialized to the specified value. 

A value of this type may be used by **IAdgTransaction** and database providers to prioritize transaction contexts.

For the System i database provider, the value of the **TransactionLevel** property translates to the value of the "LCKLVL" parameter of the "STRCMTCTL" command used to begin a transaction context. Please consult the iSeries database documentation for details. The following table summarizes the translation. 
## Members



| Member | iSeries STRCMTCTL LCKLVL |
| ---- | ---- |
| Low | *CHG |
| Medium | *CS |
| High | *ALL |
| Serial | *ALL |



## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
## See Also


[AdgConnection Class](adg-connection-class.html)
      <br />
      [BeginTransaction 
					Method](adg-connection-class-begin-transaction-method-main.html)
      <br />
      [BeginAutoTransaction 
					Method](adg-connection-class-begin-auto-transaction-method-main.html)
      <br />
[IAdgTransaction Class](iadg-transaction-class.html)
      <br />
      [TransactionLevel 
					Property](iadg-transaction-class-transaction-level-property.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

