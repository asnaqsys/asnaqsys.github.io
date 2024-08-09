---
title: "PrintingProps class           | QSYS API Reference Guide"
description: "Represents the application settings for printing properties. This class is auto-generated and changes may be overwritten. "
last_modified_at: 2024-08-09T16:18:40Z
---

Represents the application settings for printing properties.
This class is auto-generated and changes may be overwritten.

**Namespace:** ASNA.DataGate.Client.Properties
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [SettingsBase](https://learn.microsoft.com/en-us/dotnet/api/system.configuration.settingsbase?view=net-8.0) --> [ApplicationSettingsBase](https://learn.microsoft.com/en-us/dotnet/api/system.configuration.applicationsettingsbase?view=net-8.0)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [PrintingProps](/reference/datagate/datagate-client/printing-props.html) | Default | Gets the default instance of the PrintingProps class. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Renderer | Gets the Renderer setting from the application settings. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | RenderInProc | Gets the RenderInProc setting from the application settings. |

## Methods

| Signature | Description |
| --- | --- |
| [GetRendererPath()](#string-getrendererpath) | Retrieves the Renderer path from the application settings.
| [IsRendererPathMissing()](#bool-isrendererpathmissing) | Checks if the Renderer path is missing in the application settings.
| [SetRendererPath](#void-setrendererpathstring-path-configuration-config)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Configuration](https://learn.microsoft.com/en-us/dotnet/api/system.configuration.configuration?view=net-8.0)) | Sets the Renderer path in the specified configuration.
| [SetRendererPathInMachineConfig](#void-setrendererpathinmachineconfigstring-path)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the Renderer path in the machine configuration.

### string GetRendererPath()

Retrieves the Renderer path from the application settings.


#### Remarks
This method retrieves the 'Renderer' property value from the application settings.If the property value is null or using its default value, the method returns the default Renderer path.

```cs
string GetRendererPath()
```

### bool IsRendererPathMissing()

Checks if the Renderer path is missing in the application settings.


#### Remarks
This method checks the 'Renderer' property value in the application settings.If the property value is null, using its default value, or equal to the default value, the method returns true.Otherwise, it returns false.

```cs
bool IsRendererPathMissing()
```

### void SetRendererPath([string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Configuration config](https://learn.microsoft.com/en-us/dotnet/api/system.configuration.configuration?view=net-8.0))

Sets the Renderer path in the specified configuration.


#### Remarks
This method sets the 'Renderer' property value in the specified configuration.It retrieves the 'appSettings' section from the configuration, and then sets the new Renderer path.

```cs
void SetRendererPath(string path, Configuration config)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The new Renderer path.
| [Configuration](https://learn.microsoft.com/en-us/dotnet/api/system.configuration.configuration?view=net-8.0) | config | The configuration in which to set the Renderer path.

### void SetRendererPathInMachineConfig([string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the Renderer path in the machine configuration.


#### Remarks
This method sets the 'Renderer' property value in the machine configuration.It opens the machine configuration, and then calls the SetRendererPath method to set the new Renderer path.

```cs
void SetRendererPathInMachineConfig(string path)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The new Renderer path.
