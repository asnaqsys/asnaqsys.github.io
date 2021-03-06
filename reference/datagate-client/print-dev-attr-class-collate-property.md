---
title: PrintDevAttr.Collate Property

Id: dcsPrintDevAttrClassCollateProperty
TocParent: dcsPrintDevAttrProperties
TocOrder: 0

keywords: Collate property
keywords: PrintDevAttr.Collate property
keywords: printing, collate multiple copies
keywords: printer device parameters, collate multiple copies
keywords: printers, device parameters, collate
keywords: collate copies, about
keywords: copies, collate
keywords: how to, collate multiple copies

---

The **Collate** property indicates the output produced by capable printers should be collated when this property is set to **True** .
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public bool Collate { get; set; }** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property Collate As Boolean** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Collate Access(*Public) Type(*Boolean)
   BegGet,   BegSet** 
      </pre>

## Property Value

Boolean. Returns or sets a value indicating whether the printed output should be collated when printing multiple copies. 
## Remarks

Setting this property to True will allow multiple copies to be collated. However, this property is applicable only when printing multiple copies or when the [Copies](print-dev-attr-class-copies-property.html) property is &gt;1.
## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[PrintDevAttr Class](print-dev-attr-class.html)
      <br />
[PrintDevAttr Class Members](print-dev-attr-members.html)
      <br />
[Copies Property](print-dev-attr-class-copies-property.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

