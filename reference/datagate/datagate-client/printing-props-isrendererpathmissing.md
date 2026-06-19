---
title: "PrintingProps.IsRendererPathMissing Method"
description: "Checks if the Renderer path is missing in the application settings."
---

## Definition

**Namespace:** ASNA.DataGate.Client.Properties  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Checks if the Renderer path is missing in the application settings.

<a id="bool-isrendererpathmissing"></a>
## bool IsRendererPathMissing()

Checks if the Renderer path is missing in the application settings.

#### Remarks
This method checks the 'Renderer' property value in the application settings.If the property value is null, using its default value, or equal to the default value, the method returns true.Otherwise, it returns false.

```cs
bool IsRendererPathMissing()
```

## See Also
- [PrintingProps class](printing-props.html)
