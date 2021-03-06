---
title: As400Program.Connection Property

Id: dcsAs400ProgramClassConnectionProperty
TocParent: dcsAs400ProgramPropertiesMain
TocOrder: 0

keywords: Connection property
keywords: As400Program.Connection property

keywords: database connections, hosting AdgConnection specified
keywords: database servers, hosting connection specified
keywords: how to, specify database host connection for program

---

The **AdgConnection** object of the database server hosting the program to be called. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public [AdgConnection](adg-connection-class.html) Connection { set; }** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public WriteOnly Property Connection As [AdgConnection](adg-connection-class.html)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Connection Access(*Public) Type([AdgConnection](adg-connection-class.html))
   BegSet** 
      </pre>

## Property Value

[AdgConnection](adg-connection-class.html). Set-Only. Represents the connection to the database server hosting the program.
## Exceptions

[ASNA.DataGate.Common.dgException](dgexception-class.html) is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of 							<br /> 							dgException.Error | Condition |
| ---- | ---- |
| dgEINVARG | The reference being assigned to **Connection** is null, or is an **AdgConnection** object whose [ State](adg-connection-class-state-property.html) property is not equal to System.Data.ConnectionState.Open (see Remarks). |
| dgEmINVSQLOP | The value of **Connection** is not a valid connection for use with As400Program. |



## Remarks

To run the program on a particular database server, set the **Connection** property with an [AdgConnection](adg-connection-class.html) object containing an open connection to the machine. If **As400Program** was instantiated with the [default constructor](as400program-class-as400program-method1.html) (no parameters), this property must be set before adding program parameters or calling the [AdgConnection.Open](dcsAs400ProgramClassExecuteMethod.htm ">Execute</a> method.

**Connection** is a set-only property. If **Connection** is set with a null value or is an **AdgConnection** instance that is unconnected or incompatible with **As400Program** , an exception is raised. Use <a href="dcsAdgConnectionClassOpenMethod.html) to open a connection to an IBM i database provider prior to setting **Connection.** 
## Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  As400Program prog = new As400Program();
  prog.Connection = new AdgConnection("*Public/DG NET IBM i");
  prog.ProgramPath = "*Libl/Call400";</pre>
<pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim prog As New As400Program()
  prog.Connection = New AdgConnection("*Public/DG NET IBM i")
  prog.ProgramPath = "*Libl/Call400"</pre>
<pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  DclFld prog Type(As400Program) New()
  prog.Connection = *New AdgConnection("*Public/DG NET IBM i")
  prog.ProgramPath = "*Libl/Call400"</pre>

## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[As400Program Class](as400program-class.html)
      <br />
[As400Program Class Members](as400program-members.html)
      <br />
[AdgConnection Class](dcsAs400ProgramClassExecuteMethod.htm ">Execute Method</a>
      <br />
      <a href="dcsAdgConnectionClass.html)
      <br />
[State Property](adg-connection-class-state-property.html)
      <br />
[Open Method](adg-connection-class-open-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

