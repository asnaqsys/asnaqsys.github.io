---
title: WebDevice.SignalDataReadyForUser Method

---

Signals the **WebDevice** object thread indicate the device is ready for data from a user event.

#### Syntax
<pre class="prettyprint"> **BegSr SignalDataReadyForUser() Access(*Public) Type(Void)**      </pre> 

#### Remarks
This method is used to signal to the **WebDevice** object program thread that the device is ready for data from a user event. The thread state of the current program will be changed from "waiting" to "running" or "ready". Use [ WaitForDataForUser](web-device-class-wait-for-data-for-user-method.html) to place the thread in the 'wait' state.
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

#### See Also
[WebDevice Class](web-device-class.html) <br /> [ WebDevice Class Members](web-device-class-members.html) <br /> [ASNA.Monarch Namespace](monarch-namespace.html) 
