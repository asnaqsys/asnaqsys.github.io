---
title: "AdgConnection.GetSourceProfileCopy Method"
description: "Gets copy of connection's source profile."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll


### SourceProfile GetSourceProfileCopy()

Return a deep-copy of the current value of the connection's source profile


#### Remarks
Since the returned object is a copy, modifications to it have no effect on this AdgConnection instance.  

```cs
SourceProfile GetSourceProfileCopy()
```

#### Returns

| Type | Description
| --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | A copy of the source profile associated with the connection.


## See Also

[AdgConnection Class](adg-connection.html)