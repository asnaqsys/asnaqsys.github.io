---
title: "EditedValueProvider class     | QSYS API Reference Guide"
description: "Provides support for Posted form validation for fields with Edit Code or Edit Word. (This value provider is registered in Startup.ConfigureServices)  "
last_modified_at: 2024-08-09T16:18:58Z
---

Provides support for Posted form validation for fields with Edit Code or Edit Word. (This value provider is registered in Startup.ConfigureServices) 

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [BindingSourceValueProvider](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.bindingsourcevalueprovider?view=aspnetcore-8.0)
<br>
<br>

## Remarks

This value provider is registered in [Startup.ConfigureServices](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/startup).

## Constructors

| Name | Description |
| --- | --- |
| [EditedValueProvider](#editedvalueproviderbindingsource-iformcollection-cultureinfo)([BindingSource](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.bindingsource), [IFormCollection](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.iformcollection), [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo)) | Initializes a new instance of EditedValueProvider

### EditedValueProvider([BindingSource](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.bindingsource), [IFormCollection](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.iformcollection), [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo))

Initializes a new instance of EditedValueProvider

```cs
EditedValueProvider(BindingSource, IFormCollection, CultureInfo)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [BindingSource](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.bindingsource) | bindingSource | BindingSource for model binding
| [IFormCollection](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.http.iformcollection) | values | Parsed form request
| [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) | culture | Information about specific Culture

## Properties

| Type | Name | Description
| --- | --- | --- 
| [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) | Culture | Gets a value with Culture specific information |

## Methods

| Signature | Description |
| --- | --- |
| [ContainsPrefix](#bool-containsprefixstring-prefix)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Overrides ContainsPrefix from the base
| [GetFieldTemplateName](#string-getfieldtemplatenamestring-originalfieldname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Produce a field's name which is either the original name or if a subfile field then without the actual subfile RRN.
| [GetKeysFromPrefix](#idictionary-string-string-getkeysfromprefixstring-prefix)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a Dictionary withe the keys from a given prefix
| [GetValue](#valueproviderresult-getvaluestring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a ValueProviderResult given a dictionary key

### bool ContainsPrefix([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Overrides ContainsPrefix from the base

```cs
bool ContainsPrefix(string prefix)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix | prefix sub-string

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if string contains the given prefix

### string GetFieldTemplateName([string originalFieldName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Produce a field's name which is either the original name or if a subfile field then without the actual subfile RRN.

```cs
string GetFieldTemplateName(string originalFieldName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | originalFieldName | Original qualified field name.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Return field's name without an actual subfile RRN.

### IDictionary\<string, string\> GetKeysFromPrefix([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a Dictionary withe the keys from a given prefix

```cs
IDictionary<string, string> GetKeysFromPrefix(string prefix)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix | input prefix

#### Returns

| Type | Description
| --- | ---
| [IDictionary`2](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2) | A Dictionary with a string key with string elements

### ValueProviderResult GetValue([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a ValueProviderResult given a dictionary key

```cs
ValueProviderResult GetValue(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | input dictionary key

#### Returns

| Type | Description
| --- | ---
| [ValueProviderResult](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.valueproviderresult?view=aspnetcore-8.0) | the value provider result
