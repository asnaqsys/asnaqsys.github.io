---
title: "AdgConnection Constructors"
description: "Initializes a new instance of the AdgConnection class."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the AdgConnection class.

## Overloads

| Name | Description |
| --- | --- |
| [AdgConnection](#adgconnectionsourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the AdgConnection class with the specified SourceProfile.
| [AdgConnection](#adgconnectionsourceprofile-iexchange5250)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html)) | Initializes a new instance of the AdgConnection class with the specified SourceProfile and IExchange5250.


### AdgConnection([SourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Initializes a new instance of the AdgConnection class with the specified SourceProfile.

```cs
AdgConnection(SourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The SourceProfile to be used for the connection.

#### Remarks

An **AdgConnection** object is constructed by specifying an initial value for the `SourceProfile` property, which is subsequently used by the `Open` method to connect to a particular database server. The properties of **SourceProfile** specify the database connection parameters.

### AdgConnection([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html))

Initializes a new instance of the AdgConnection class with the specified SourceProfile and IExchange5250.

```cs
AdgConnection(SourceProfile, IExchange5250)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The SourceProfile to be used for the connection.
| [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html) | exchange5250 | The IExchange5250 to be used for the connection.



## See Also

[AdgConnection Class](adg-connection.html)