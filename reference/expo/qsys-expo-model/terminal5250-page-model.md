---
title: "Terminal5250_PageModel class  | QSYS API Reference Guide"
description: "Defines Terminal5250_PageModel class "
last_modified_at: 2024-08-09T16:18:58Z
---

Defines Terminal5250_PageModel class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [PageModel](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.razorpages.pagemodel?view=aspnetcore-8.0) --> [YellowPageModel](/reference/expo/qsys-expo-model/yellow-page-model.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Terminal5250_PageModel()](#terminal5250-pagemodel) | Initializes a new instance of Terminal5250_PageModel class

### Terminal5250_PageModel()

Initializes a new instance of Terminal5250_PageModel class

```cs
Terminal5250_PageModel()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [From5250Screen_Model](/reference/expo/qsys-expo-model/from5250-screen-model.html) | From5250Screen | Gets sets an instance to From5250Screen_Model object |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InputDataAvailable | Implements required override by returning true |
| [To5250Screen_Model](/reference/expo/qsys-expo-model/to5250-screen-model.html) | To5250Screen | Gets sets an instance to To5250Screen_Model object |

## Methods

| Signature | Description |
| --- | --- |
| [ClearModelProperties()](#void-clearmodelproperties) | Clears Model Properties
| [DumpModelPropertiesToDataSet()](#void-dumpmodelpropertiestodataset) | Dumps model's properties to the DataSet
| [LoadModelPropertiesFromDataSet](#void-loadmodelpropertiesfromdatasetbool-onlynonpostedfields)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Loads model's properties from the DataSet
| [MyAjaxActionResult()](#jsonresult-myajaxactionresult) | Gets the AJAX JSON result
| [MyAjaxActionResult](#jsonresult-myajaxactionresultredirectedexception-redirect)([RedirectedException](/reference/expo/qsys-expo-model/redirected-exception.html)) | Gets the AJAX JSON result with redirect URL
| [SetResponseIndicators()](#void-setresponseindicators) | Implements the required ovveride by doing nothing: There are no Response Indicators for 5250.

### void ClearModelProperties()

Clears Model Properties

```cs
void ClearModelProperties()
```

### void DumpModelPropertiesToDataSet()

Dumps model's properties to the DataSet

```cs
void DumpModelPropertiesToDataSet()
```

### void LoadModelPropertiesFromDataSet([bool onlyNonPostedFields](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Loads model's properties from the DataSet

```cs
void LoadModelPropertiesFromDataSet(bool onlyNonPostedFields)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | onlyNonPostedFields | indicates what to laod

### JsonResult MyAjaxActionResult()

Gets the AJAX JSON result

```cs
JsonResult MyAjaxActionResult()
```

### JsonResult MyAjaxActionResult([RedirectedException redirect](/reference/expo/qsys-expo-model/redirected-exception.html))

Gets the AJAX JSON result with redirect URL

```cs
JsonResult MyAjaxActionResult(RedirectedException redirect)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [RedirectedException](/reference/expo/qsys-expo-model/redirected-exception.html) | redirect | redirected exception instance

#### Returns

| Type | Description
| --- | ---
| [JsonResult](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.jsonresult?view=aspnetcore-8.0) | JsonResult serialized respose

### void SetResponseIndicators()

Implements the required ovveride by doing nothing: There are no Response Indicators for 5250.

```cs
void SetResponseIndicators()
```
