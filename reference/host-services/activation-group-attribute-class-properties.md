---
title: ActivationGroupAttribute Properties

---

[ ActivationGroupAttribute Overview](activation-group-attribute-class.html) 
<!-- start public properties table -->	

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Property</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr valign="top">
            <td>              <img class="hcp4" style="WIDTH: 16px; HEIGHT: 16px" height="16" alt="public property" src="images/property.bmp" width="16" border="0" />
              [
              GroupName](activation-group-attribute-class-group-name-property.html)
            </td>
            <td

>Gets a string value
            containing the name of the activation
            group to use for the program.</td>
          </tr>
          <tr>
            <td>              ![](images/property.bmp)
              [
              IsCaller](activation-group-attribute-classIs-caller-property.html)
            </td>
            <td>Gets a boolean value
            indicating whether the program will be allocated in the
            same activation group as the program calling this
            program. The default is 
 **False** .</td>
          </tr>
          <tr>
            <td>              ![](images/property.bmp)
              [
              IsDefault](activation-group-attribute-classIs-default-property.html)
            </td>
            <td>Gets a boolean value
            indicating whether the program falls into the *Default
            activation group.  Those without an
            ActivationGroup attribute are allocated to this
            group. The default is 
 **True** .</td>
          </tr>
          <tr>
            <td>              ![](images/property.bmp)
              [
              IsNew](activation-group-attribute-classIs-new-property.html)
            </td>
            <td

>Gets a boolean value
            indicating whether the program is to be run in a new
            activation group. The default is 
 **False** .</td>
          </tr>
</table>

#### See Also
[ ActivationGroupAttribute Class](activation-group-attribute-class.html) <br clear="none" /> [ASNA.Monarch Namespace](monarch-namespace.html) 
