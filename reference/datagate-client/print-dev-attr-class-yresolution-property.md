---
title: PrintDevAttr.YResolution Property

---

The **YResolution** specifies the y-axis resolution (in dots-per-inch) when printing graphics.

```cs
 public int YResolution { get; set; }
```


## Property Value

Integer. Returns or sets a value that defines the resolution in which graphics will be printed. 
## Remarks

Printers support one or more horizontal and vertical resolutions for faster graphics output. A resolution is an integer value specified in dots-per-inch (dpi), which indicates the number of distinct dots that the print head or inkjet can apply along the x- or the y-axis.

Typically, the x-y resolutions will be the same, such as300 x 300, or 600 x 600, etc. Since the x-y resolutions are the same, you only need to specify one resolution.
## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[PrintDevAttr Class](print-dev-attr-class.html)
      <br />
[PrintDevAttr Class Members](print-dev-attr-members.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

