---
title: "DisplayPagesOptions class     | QSYS API Reference Guide"
description: "Provides configuration for Display Pages. "
last_modified_at: 2024-08-09T17:26:04Z
---

Provides configuration for Display Pages.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

Website Applications using `ASNA.QSys.Expo` assembly, typically have a configuration file at the root folder of the site named: `appsettings.json`.

The configuration file `appsettings.json` uses [JSON](https://www.json.org/json-en.html) file format.

There is a `"DisplayPages"` object defined in the schema for `appsettings.json`, where the Properties described by this class can be set to configure the Website. 


## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FakeDataDirectory | File system absolute path holding test data for testing Display Pages.Defaults to the "/temp/FakeData" directory. |
| [FakeDataType](/reference/expo/qsys-expo-model/fake-data-type.html) | FakeDataType | Controls the generation and/or use of Fake data in lieu of running the program's logic.Defaults to none, when set to a different value, the value of "FakeDataDirectory" is used to locate the Fake data. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | MultiJobOnBrowser | Determines if multiple jobs are supported for the same browser |
