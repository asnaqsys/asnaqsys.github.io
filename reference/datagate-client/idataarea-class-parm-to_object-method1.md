---
title: IDataArea.ParmToObject(ASNA.DataGate.DataLink.ProgParm, System.Type)

Id: dcsIDataAreaClassParmToObjectMethod1
TocParent: dcsIDataAreaClassParmToObjectMethods
TocOrder: 51

---

Returns an object of a specific type from the program parameter list provided with the program parameter object in the parameter list to get the value of and the type of the object returned by the method.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public object ParmToObject(
[ASNA.DataGate.Client](DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a> Parameter,
   System.Type ReturnType
);** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function ParmToObject(_ 
   ByVal Parameter As <a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a> _
   ByVal ReturnType As System.Type
) As Object** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ParmToObject Access(*Public) Type(Object)
   DclSrParm Parameter Type(<a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a>)
   DclSrParm ReturnType Type(System.Type)** 
      </pre>

## Parameters

<dl>
        <dt>
 *Parameter* 
        </dt>
        <dd><a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a>.  
						The program parameter object in the parameter list to get the value of.</dd>
        <dt>
 *ReturnType* 
        </dt>
        <dt />
        <dd>			System.Type.  The requested type of the object returned by the method.</dd>
</dl>

## Requirements

**Namespace:** <a href="dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IDataArea Class](idataarea-class.html)
      <br />
[IDataArea Class Members](dcsIDataAreaMembers.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

