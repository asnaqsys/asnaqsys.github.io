---
title: FieldType.Scale Property

Id: dcsFieldTypeClassScaleProperty
TocParent: dcsFieldTypeProperties
TocOrder: 5

keywords: Scale property
keywords: FieldType.Scale property
keywords: decimal fields, maximum number of digits to right of decimal point
keywords: fields, maximum number of digits to right of decimal point
keywords: maximum number of digits to right of decimal point
keywords: how to, define maximum number of digits to right of decimal point
keywords: number of, maximum digits to right of decimal point

---

The maximum number of digits to the right of the decimal point (for decimal fields only).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int Scale { get; }**  </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Scale**  </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Scale Type(*Integer) Len(4) Access(*Public)<br />   BegGet** 
      </pre>

## Property Value

Integer. Returns the maximum number of digits to the right of the decimal point (for decimal fields only).
## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FieldType Class](field-type-class.html)
      <br />
[FieldType Class Members](field-type-members.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

