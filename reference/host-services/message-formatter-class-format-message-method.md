---
title: MessageFormatter.FormatMessage Method

---

Returns a formatted message.

#### Syntax
<pre class="syntax"> **BegFunc FormatMessage Access(*Public) Type(*String)
   DclSrParm *msgFilePath*   Type(*String)
   DclSrParm *message*  Type(ASNA.Monarch.Message)** </pre>  

#### Parameters
<dl>
        <dt>
 *msgFilePath* 
        </dt>
        <dd>String. The file path for the message being
        formatted.</dd>
        <dt>
 *message* 
        </dt>
        <dd>An instance of an 
        [
        ASNA.Monarch.Message](message-class.html) object being
        formatted.</dd>
</dl> 

<!--mine -->

#### Return Value
String. The formatted message.
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="60%">
          <colgroup>
            <col width="30%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>
          <tr>
            <td>InvalidMesssageFormatException</td>
            <td>The message file is not
            properly formatted.</td>
          </tr>
          <tr />
</table>

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
            <td>ASNA.Monarch.WebDspF.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ MessageFormatter Class](message-formatter-class.html) <br /> [ MessageFormatter Class Members](message-formatter-members.html) <br /> [ ASNA.Monarch.Message Class](message-class.html) <br />[ASNA.Monarch Namespace](monarch-namespace.html)
