---
title: CLProgram.RetrieveDataArea(string)

---

Returns the local data area associated with the job.

#### Syntax
<pre class="syntax"> **BegFunc RetrieveDataArea Access(*Protected) Type(*String)
   DclSrParm *dataArea*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *dataArea* </code>
        </dt>
        <dd>String. The path to the data area to retrieve.</dd>
</dl>

#### Return Value
String. Variable containing the contents of the local *dataArea* .

#### Remarks
If you want to retrieve many subfields, use this method and then use <code>[ Percent_SST](clprogram-class-percent-sst-method.html)</code> to extract subfields.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](monarch-namespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](clprogram-class.html) <br clear="none" /> [ CLProgram Class Members](clprogram-class-members.html) <br clear="none" /> [Percent_SST Method](clprogram-class-percent-sst-method.html) <br clear="none" /> [ASNA.Monarch Namespace](monarch-namespace.html) 
