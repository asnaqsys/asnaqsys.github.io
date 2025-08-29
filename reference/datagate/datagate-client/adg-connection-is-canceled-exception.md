---
title: "AdgConnection.IsCanceledException Method"
description: "Determines whether the specified exception is due to a cancellation request."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll


### bool IsCanceledException([Exception e](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Determines whether the specified exception is due to a cancellation request.


#### Remarks
This method checks if the cancellation token for the connection is CancellationToken.None.If it is, it returns false, because a cancellation request could not have been made.If the cancellation token is not CancellationToken.None, it calls the IsCanceledExceptionInternal method to check if the specified exception is due to a cancellation request.

```cs
bool IsCanceledException(Exception e)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | The exception to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified exception is due to a cancellation request; otherwise, false.


## See Also

[AdgConnection Class](adg-connection.html)