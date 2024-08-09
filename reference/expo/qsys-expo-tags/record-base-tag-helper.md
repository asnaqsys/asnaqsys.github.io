---
title: "RecordBaseTagHelper class     | QSYS API Reference Guide"
description: "Provides common properties for DdsRecords "
last_modified_at: 2024-08-09T16:19:09Z
---

Provides common properties for DdsRecords

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

There are three Display Records in QSys.Expo, namely: [DdsRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html), [DdsSubfileControl](/reference/expo/qsys-expo-tags/dds-subfile-control-tag-helper.html) and [DdsSubfileRecord](/reference/expo/qsys-expo-tags/dds-subfile-record-tag-helper.html) Tag Helpers. These three Tag Helpers derive directly (or indirectly) from the `RecordBaseTagHelper` [abstract class](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members).

Common properties and methods for the Display Records are defined in class `RecordBaseTagHelper`.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ModelExpression](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.viewfeatures.modelexpression) | For | Gets or sets the Model reference to the Record class. Mostly to simplify markup syntax.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormatName | Gets the value indicating the name of the Record format. |
| [RecordModel](/reference/expo/qsys-expo-model/record-model.html) | RecordModel | Gets or sets RecordModel associated with the Record tag helper |
