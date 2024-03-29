---
title: WebDisplayFile.Read Method

---

Reads an array of characters in the **WebDisplayFile** object by the specified indicators.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegSr Read Access(*Public) Type(Void)
   DclSrParm *indicators*  Type(*Char) Rank(1)** </code></pre>

#### Parameters
<dl>
        <dt>
          <code> *indicators* </code>
        </dt>
        <dd>The indicators specified.</dd>
</dl>

<!--mine -->

#### Exceptions
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>          <tr>
            <td>
            <code>NoDeviceAvailableException</code></td>
            <td>The web device could not be
            found.</td>
          </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch](monarch-namespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ WebDisplayFile Class](web-display-file-class.html) <br /> [ WebDisplayFile Class Members](web-display-file-class-members.html) <br /> [ASNA.Monarch Namespace](monarch-namespace.html)
