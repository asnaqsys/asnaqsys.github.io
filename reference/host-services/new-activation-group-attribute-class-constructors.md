---
title: NewActivationGroupAttribute.NewActivationGroupAttribute Constructor()

---

This method constructs a new instance of a **NewActivationGroupAttribute** object.
<pre class="prettyprint"> **BegConstructor NewActivationGroupAttribute() Access(*Public)**       </pre>

#### Remarks
Using **NewActivationGroupAttribute** defines an instance when the activation group for the program is to be run in a new activation group. Monarch will create a new unique name for the group. An example of the BegClass follows.
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes ( NewActivationGroup ())</pre>

Refer to [ ActivationGroupAttribute Class](activation-group-attribute-class.html) and [ CallerActivationGroupAttribute Class](caller-activation-group-attribute-class.html) for more information.
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
[ NewActivationGroupAttribute Class](new-activation-group-attribute-class.html)<br />[ NewActivationGroupAttribute Class Members](new-activation-group-attribute-class-members.html)<br />[ASNA.Monarch Namespace](monarch-namespace.html)
