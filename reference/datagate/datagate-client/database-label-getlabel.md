---
title: "DatabaseLabel.GetLabel Method"
description: "Retrieves a specific label from a given server."
---

## Definition

**Namespace:** ASNA.DataGate.Client.DatabaseLabel  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Retrieves a specific label from a given server.

<a id="ilabel-getlabel-sourceprofile-sp-string-lblname"></a>
## ILabel GetLabel(SourceProfile sp, string lblName)

Retrieves a specific label from a given server.

#### Remarks
This method uses the  method to retrieve all labels from the server specified in the source profile.It then uses LINQ to filter the labels based on the provided name, using a case-insensitive comparison.If a label with the provided name is found, it is returned; otherwise, the method returns null.

```cs
ILabel GetLabel(SourceProfile sp, string lblName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The source profile containing server and user credentials.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | lblName | The name of the label to retrieve.

#### Returns

| Type | Description
| --- | ---
| [ILabel](/reference/datagate/datagate-client/i-label.html) | The label matching the provided name, or null if no match is found.

## See Also
- [DatabaseLabel class](database-label.html)
