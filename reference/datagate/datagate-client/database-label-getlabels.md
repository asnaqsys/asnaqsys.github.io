---
title: "DatabaseLabel.GetLabels Method"
description: "Creates a list of all labels in a given server"
---

## Definition

**Namespace:** ASNA.DataGate.Client.DatabaseLabel  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a list of all labels in a given server

<a id="ilabel-getlabels-sourceprofile-sp"></a>
## ILabel\[\] GetLabels(SourceProfile sp)

Creates a list of all labels in a given server

```cs
ILabel[] GetLabels(SourceProfile sp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | Connection parameters defining the machine to            to search, server TCP port, user credentials, and Krb5 SPN.            

#### Returns

| Type | Description
| --- | ---
| [ILabel\[\]](/reference/datagate/datagate-client/i-label.html) | Array of labels

## See Also
- [DatabaseLabel class](database-label.html)
