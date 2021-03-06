---
title: AdgConnection.op_InEquality Method

Id: dcsAdgConnectionClassopInequalityMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 8

keywords: op_InEquality method
keywords: AdgConnection.op_InEquality method

keywords: comparing two AdgConnection objects
keywords: how to, compare two AdgConnection objects

---

Returns the opposite value returned by [op_Equality](adg-connectionclassop-equality-method.html).
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **AdgConnection.op_Inequality(x, y)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual Basic]</span>
 **returnValue = AdgConnection.op_Inequality(x, y)** 
      </pre>

## Parameters

<dl>
        <dt>
 *x* 
        </dt>
        <dd>An **AdgConnection**  object to compare. </dd>
        <dt>
 *y* 
        </dt>
        <dd>An **AdgConnection**  object to compared.</dd>
</dl>

## Exceptions

None.
## Remarks

Returns **false** if the references being compared refer to the same object. Otherwise, returns the negated value of the [Equals](adg-connection-class-equals-method.html) method invoked on left, and passed right as a parameter. 
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgConnection Class](adg-connection-class.html)
      <br />
[AdgConnection Class Members](adg-connection-members.html)
      <br />
[Equals Method](adg-connection-class-equals-method.html)
      <br />
[Op_Equality Method](adg-connectionclassop-equality-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

