---
title: IPrintProperties.SetValue Method

Id: dcsIPrintPropertiesClassSetValueMethod
TocParent: dcsIPrintPropertiesMethods
TocOrder: 3

keywords: SetValue method
keywords: IPrintProperties.SetValue method
keywords: print controls, format fields, property value set
keywords: print controls, run time properties set
keywords: print files, set print control property values

---

Assign a value to a print control property.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void SetValue(
   fieldName string,
   propName string,
   object val
);** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public sub SetValue( _
  ByVal fieldName As string _
  ByVal propName As string _
  ByVal val as object _
) As Void** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr SetValue Type(Void) Access(*Public)
   DclSrParm fieldName Type(*string)
   DclSrParm propName Type(*string)
   DclSrParm val Type (*object)** 
      </pre>

## Parameters

<dl>
        <dt>
 *fieldName* 
        </dt>
        <dd>
 **String** .  The field in the format represented by **IPrintProperties** 
						associated with the print control. </dd>
        <dt>
 *propName* 
        </dt>
        <dd>
 **String** .  The property name of the print control to obtain 
								the value of.  </dd>
        <dt>
 *val* 
        </dt>
        <dd>
 **Object** .  The value to assign to the property.
									</dd>
</dl>

## Exceptions



| Exception Type | Condition |
| ---- | ---- |
|  | <p>The property specified by *propName* cannot be found for the control of the field specified by *fieldName* . |
| NullReferenceException | *fieldName* or *propName* is a null reference. |



## Remarks

Print controls associated with format fields have run-time properties that can be assigned with **SetValue** . **IPrintProperties** refers to the format containing the field with associated print control, *fieldName* refers to the field, and *propName* is the name of a property of the control. The value assigned to the property is passed as *val* .

Since print controls may be implemented as COM-based unmanaged objects, this method may invoke .NET interoperability functions to obtain a so-called "runtime callable wrapper" for such controls. The user should be aware of the constraints of .NET interoperability in terms of performance and security when using this method.

As a convenience, **SetValue** performs a simple conversion for certain OLE class types representing image data. If *val* is of type **System.Drawing.Image** , then DCS uses .NET framework classes to convert the value to the **stdole.IPicture** type. The **Image** class is somewhat more useful for .NET programs and objects of the type are readily convertible to one of the OLE interop types if necessary. 
## Requirements

<span> **Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> Pro
## See Also


[IPrintProperties Class](iprint-properties-class.html)
      <br />
      [
					MissingFieldException Class Topic](ms-help://MS.VSCC.2003/MS.MSDNQTR.2003FEB.1033/cpref/html/frlrfSystemMissingfieldexceptionClassTopic.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

