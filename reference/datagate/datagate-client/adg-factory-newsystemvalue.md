---
title: "AdgFactory.NewSystemValue Method"
description: "Creates a new instance of the interface."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new instance of the interface.

<a id="isystemvalue-newsystemvalue-adgconnection-cn-bool-withnewtransaction"></a>
## ISystemValue NewSystemValue(AdgConnection cn, bool withNewTransaction)

Creates a new instance of the  interface.

#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
ISystemValue NewSystemValue(AdgConnection cn, bool withNewTransaction)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | withNewTransaction | A boolean value indicating whether to create a new transaction.

#### Returns

| Type | Description
| --- | ---
| [ISystemValue](/reference/datagate/datagate-client/i-system-value.html) | A new instance of the  interface.

## See Also
- [AdgFactory class](adg-factory.html)
