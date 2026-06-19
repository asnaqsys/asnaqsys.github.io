---
title: "DatabaseLabel class"
description: "The `DatabaseLabel` class provides static methods for managing and interacting with database labels in a DataGate environment. "
last_modified_at: 2024-08-09T17:25:07Z
---

The `DatabaseLabel` class provides static methods for managing and interacting with database labels in a DataGate environment.

**Namespace:** ASNA.DataGate.Client.DatabaseLabel
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
This class includes methods for creating, changing, and removing databases, as well as retrieving and manipulating labels.
Labels are used to identify and manage databases in the DataGate environment. They can be retrieved either individually, by name, or as a collection.
The class also provides methods for labeling and unlabeling databases, and for creating new label objects.

<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ChangeDatabase](database-label-changedatabase.html#void-changedatabase-sourceprofile-serverandcredentials-ilabel-label)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [ILabel](/reference/datagate/datagate-client/i-label.html)) | Modifies database label
| [CreateDatabase](database-label-createdatabase.html#void-createdatabase-sourceprofile-serverandcredentials-bool-bissecured-ilabel-label)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ILabel](/reference/datagate/datagate-client/i-label.html)) | Creates a database
| [CreateDatabase](database-label-createdatabase.html#void-createdatabase-sourceprofile-serverandcredentials-bool-bissecured-ilabel-plabel-int-tcpport)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ILabel](/reference/datagate/datagate-client/i-label.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a database
| [CreateLabelObject()](database-label-createlabelobject.html#ilabel-createlabelobject) | Creates an ILabel object with default values
| [GetLabel](database-label-getlabel.html#ilabel-getlabel-sourceprofile-sp-string-lblname)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves a specific label from a given server.
| [GetLabels](database-label-getlabels.html#ilabel-getlabels-sourceprofile-sp)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Creates a list of all labels in a given server
| [LabelDatabase](database-label-labeldatabase.html#void-labeldatabase-sourceprofile-serverandcredentials-ilabel-label-boolean-bexists)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [ILabel](/reference/datagate/datagate-client/i-label.html), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Create a label for an existing database
| [RemoveDatabase](database-label-removedatabase.html#void-removedatabase-sourceprofile-sourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Completely erases a database and its label.
| [UnlabelDatabase](database-label-unlabeldatabase.html#void-unlabeldatabase-sourceprofile-source)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Remove a label on a database

