---
title: "EditedValueProviderFactory class"
description: "Provides an Edited Value Provider factory "
last_modified_at: 2024-08-09T17:26:04Z
---

Provides an Edited Value Provider factory

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

Used internally by Website Runtime to instance [EditedValueProvider](/reference/expo/qsys-expo-model/edited-value-provider.html).

## Methods

| Signature | Description |
| --- | --- |
| [CreateValueProviderAsync](#task-createvalueproviderasyncvalueproviderfactorycontext-context)([ValueProviderFactoryContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.valueproviderfactorycontext?view=aspnetcore-8.0)) | Gets an asynchronous operation to add an Edited Value Provider to bind the model to a requested http form.

### Task CreateValueProviderAsync([ValueProviderFactoryContext context](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.valueproviderfactorycontext?view=aspnetcore-8.0))

Gets an asynchronous operation to add an Edited Value Provider to bind the model to a requested http form.

```cs
Task CreateValueProviderAsync(ValueProviderFactoryContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ValueProviderFactoryContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.valueproviderfactorycontext?view=aspnetcore-8.0) | context | Input Value Provider Factory context.

#### Returns

| Type | Description
| --- | ---
| [Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.taskscheduler) | The asynchronous operation.
