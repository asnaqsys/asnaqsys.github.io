---
title: "PrintingProps.SetRendererPathInMachineConfig Method"
description: "Sets the Renderer path in the machine configuration."
---

## Definition

**Namespace:** ASNA.DataGate.Client.Properties  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the Renderer path in the machine configuration.

<a id="void-setrendererpathinmachineconfig-string-path"></a>
## void SetRendererPathInMachineConfig(string path)

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

## See Also
- [PrintingProps class](printing-props.html)
