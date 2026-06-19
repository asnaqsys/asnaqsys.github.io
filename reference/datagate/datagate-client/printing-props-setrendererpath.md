---
title: "PrintingProps.SetRendererPath Method"
description: "Sets the Renderer path in the specified configuration."
---

## Definition

**Namespace:** ASNA.DataGate.Client.Properties  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the Renderer path in the specified configuration.

<a id="void-setrendererpath-string-path-configuration-config"></a>
## void SetRendererPath(string path, Configuration config)

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

## See Also
- [PrintingProps class](printing-props.html)
