---
title: WebDisplayFile.Write Method

---

Writes a record to a Monarch workstation file, database file, or printer file.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegSr Write() Access(*Public) Type(Void)** </code></pre>

#### Remarks
One record for each 'write'.
<!-- start -->

#### Example
Two files, a workstation file (SPD100D) and a Database file (PS335101) both can be written to.
<pre class="prettyprint"> //      *‚Display file DclWorkStnFile SDP100D DspFile ("~\Mon31120View\SDP100D.aspx") Subfile ( sfl01,#RRN )

 //     disk file DclDiskFile PS335l01 Type (*Update) AddRec (*Yes) Org (*Indexed) +     
 DB (MyJob.MyDatabase) File ("*LIBL/PS305l01") ImpOpen (*No) RnmFmt ( PS333R )        
   . . .            
 Write sfl01
   . . .
 Write PS333R</pre>

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
[ WebDisplayFile Class](web-display-file-class.html) <br /> [ WebDisplayFile Class Members](web-display-file-class-members.html) <br /> [ASNA.Monarch Namespace](monarch-namespace.html)
