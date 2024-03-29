---
title: LocalDataCollection.this Property

---

Gets or sets the collection element with the specified name.

#### Property Values
<pre class="prettyprint"> **BegProp this Access(*Public) Type(*Object) 
   DclSrParm *name*  Type(*String)
 BegGet;   BegSet;**       </pre>

#### Parameters
<dl>
        <dt>
 *name* 
        </dt>
        <dd>

String used as a string value (key) of the element to get or set.
</dd>
</dl>

#### Property Values
The element with the specified name.

#### Remarks
This property provides the ability to access a specific element in the collection.

When setting the property, if the specific name already exists in the dictionary, the value is replaced; otherwise, a new element is created. In contrast, the [Add](local-data-collection-class-add-method.html) method does not modify existing elements.
<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](monarch-namespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ LocalDataCollection Class](local-data-collection-class.html) <br /> [ LocalDataCollection Members](local-data-collection-members.html) <br /> [Add Method](local-data-collection-class-add-method.html) <br /> [ASNA.Monarch Namespace](monarch-namespace.html) 
