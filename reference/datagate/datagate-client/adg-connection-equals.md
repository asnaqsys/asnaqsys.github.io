---
title: "AdgConnection.Equals Method"
description: "Determines whether the current AdgConnection instance is equal to the specified object."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the current AdgConnection instance is equal to the specified object.

#### Remarks
This method checks if the specified object is an AdgConnection and if its SourceProfile is equal to the SourceProfile of the current instance.

Returns  false if _obj_ refers to a null instance.  Otherwise returns the value of the [op_Equality](/reference/datagate/datagate-providers/source-profile.html#bool-equalssourceprofile-other) method invoked on the **SourceProfile** proprety of this **AdgConnection** object against the **SourceProfile** of the **AdgConnection** object being compared.  

The SourceProfile is a property that contains the configuration settings for the connection, such as the database name, server name, and other connection parameters.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current instance.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is an AdgConnection and its SourceProfile is equal to the SourceProfile of the current instance; otherwise, false.



## See Also

[AdgConnection Class](adg-connection.html)