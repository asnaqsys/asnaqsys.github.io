---
title: PrintDevAttr.Orientation Property

Id: dcsPrintDevAttrClassOrientationProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 8

keywords: Orientation property
keywords: PrintDevAttr.Orientation property
keywords: PaperOrientation enumeration, used by
keywords: enumerations [DCS 16.0 PaperOrientation, used by
keywords: portrait orientation
keywords: landscape orientation
keywords: printing, orientation, about this property
keywords: printing, orientation, portrait
keywords: printing, orientation, landscape
keywords: printer device parameters, orientation
keywords: printers, device parameters, orientation
keywords: how to, determine printing orientation
keywords: print orientation, set/return values
keywords: print orientation, about

---

The **Orientation** property specifies the landscape/portrait orientation of paper in the printer. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public PaperOrientation Orientation { get; set; }** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Orientation As [PaperOrientation](paper-orientation-enumeration.html)** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Orientation Type(PaperOrientation) Access(*Public) <br />    BegGet,    BegSet** 
      </pre>

## Property Value

[ASNA.DataGate.Common.PaperOrientation](paper-orientation-enumeration.html). Returns or sets an integer value indicating the orientation of the paper in the printer. 
## Remarks

The paper orientation can be set to either <span style="FONT-WEIGHT: bold">Portrait</span> or <span style="FONT-WEIGHT: bold">Landscape</span> orientation.

<span style="FONT-WEIGHT: bold">Portrait</span> - The paper height is greater than the width.

<span style="FONT-WEIGHT: bold">Landscape - </span>The paper width is greater than the height. 
## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[PrintDevAttr Class](print-dev-attr-class.html)
      <br />
[PrintDevAttr Class Members](print-dev-attr-members.html)
      <br />
[PaperOrientation Enumeration](paper-orientation-enumeration.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

