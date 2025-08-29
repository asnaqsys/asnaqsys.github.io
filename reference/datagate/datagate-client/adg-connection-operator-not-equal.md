---
title: "AdgConnection.op_Inequality Method, AKA Operator !="
description: "Determines whether two AdgConnection instances are not equal."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### bool op_Inequality([AdgConnection x](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection y](/reference/datagate/datagate-client/adg-connection.html))

Determines whether two AdgConnection instances are not equal.


#### Remarks

Returns **false** if the references being compared refer to the same object.  Otherwise, returns the negated value of the [Equals](/reference/datagate/datagate-client/adg-connection-equals.html) method invoked on left, and passed right as a parameter.


```cs
bool op_Inequality(AdgConnection x, AdgConnection y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | x | The first AdgConnection to compare.
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | y | The second AdgConnection to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the two AdgConnection instances are not equal; otherwise, false.



## See Also

[AdgConnection Class](adg-connection.html)