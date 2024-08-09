---
title: "DisplayOptionsServiceCollectionExtensions class"
description: "Provides helper class to assist server configuration "
last_modified_at: 2024-08-09T16:18:58Z
---

Provides helper class to assist server configuration

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

ASP.NET [RazorPage](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/) Websites normally has a configuration source C# file named `Startup.cs` which is called by the ASP.NET runtime. It looks something like the following code:

```cs
public void ConfigureServices(IServiceCollection services)
{
    .
    .
    .

    services.ConfigureDisplayPagesOptions(Configuration);

```

This bootstrap [Dependency Injection](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions/hands-on-labs/aspnet-mvc-4-dependency-injection) mechanism, glues (injects) the settings of the Website file `appsettings.json`, in particular the Section `DisplayPages` to the Website configuration.

>See related class [DisplayPagesOptions Class](/reference/expo/expo-model/display-pages-options.html)


## Methods

| Signature | Description |
| --- | --- |
| [ConfigureDisplayPagesOptions](#iservicecollection-configuredisplaypagesoptionsiservicecollection-services-iconfiguration-configuration)([IServiceCollection](https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection.iservicecollection), [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0)) | Gets 

### IServiceCollection ConfigureDisplayPagesOptions([IServiceCollection services](https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection.iservicecollection), [IConfiguration configuration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0))

Gets 

```cs
IServiceCollection ConfigureDisplayPagesOptions(IServiceCollection services, IConfiguration configuration)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IServiceCollection](https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection.iservicecollection) | services | service collection reference
| [IConfiguration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.iconfiguration?view=net-8.0) | configuration | set of key value properties

#### Returns

| Type | Description
| --- | ---
| [IServiceCollection](https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection.iservicecollection) | the service collection
