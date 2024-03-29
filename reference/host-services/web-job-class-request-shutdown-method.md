---
title: WebJob.RequestShutDown Method

---

Initiates a timed shut down request for the web job.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegSr RequestShutDown Access(*Public) Type(Void)
    DclSrParm *controlledSeconds*  Type (*Integer)**  </code></pre>

#### Parameters
<dl>
        <dt>
          <code> *controlledSeconds* </code>
        </dt>
        <dd>Integer. The number of seconds in which to begin the
        shutdown.</dd>
</dl>

#### Remarks
A shutdown ends all active programs, closes the database connections for disk and printer files, and then aborts the thread assigned to the job.
<!-- -->

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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[WebJob Class](web-job-class.html) <br /> [WebJob Class Members](web-job-class-members.html) <br /> [ASNA.Monarch Namespace](monarch-namespace.html) 
