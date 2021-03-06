---
title: As400Program.AppendParm Method

Id: dcsAs400ProgramClassAppendParmMethod
TocParent: dcsAs400ProgramMethodsMain
TocOrder: 0

keywords: AppendParm method
keywords: As400Program.AppendParm method
keywords: program parameters, append parameter to
keywords: parameter lists, append parameter to
keywords: append parameter to program parameter list
keywords: parameters, append program parameter list
keywords: how to, append parameter to program parameter list

---

Appends a parameter to the parameter list for the program.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void AppendParm(
[ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html) Parameter
);** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub AppendParm( _
   ByVal Parameter As [ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html) _
)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AppendParm Acess(*Public)
   DclSrParm Parameter Type([ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html))** 
      </pre>

## Parameters

<dl>
        <dt>
          <span> *Parameter* 
          </span>
        </dt>
        <dd>
          <span />
          <span> An instance of **ASNA.DataGate.DataLink.ProgParm**  class that represents the program parameter to append. </span>  </dd>
</dl>

## Exceptions

ArgumentException. A **ProgParm** in the array has the same name as another parameter in the parameter list.<span />
## Remarks

To create a program parameter list, <span> **ProgParm** </span> objects should be added with the <span> **AppendParm** </span> or [AppendParms](as400program-class-append-parms-method.html) method in the order of their occurrence in the program parameter list. <span> **AppendParm** </span> appends a single <span> **ProgParm** </span> object to the parameter list.

The **ProgParm** appended to the list may optionally be named via the <span>name</span> parameter of the [DataLink.ProgParmType](prog-parm-type-class-prog-parm-type-constructor.html) and [DataLink.StructuredType](structure-type-class.html) constructors. If the <span> **ProgParm** </span> is named and a previously appended **ProgParm** has the same name, an ArgumentException is raised. 

**Note** that the parameter list may be constructed with this method before the [ Connection](as400program-class-connection-property.html) property has been set, but the values of the parameters may not be accessed with [ObjectToParm](as400program-class-object-to_parm-method-main.html) and [ParmToObject Method](as400program-class-parm-to_object-method-main.html) until <span> **Connection** </span> has a value.
## Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here, prog is an initialized As400Program.
   * We add the field "CustName" to the parm list, and a local
   * string variable by the same name into it.  After calling the
   * program, we then set the local variable to the returned
   * value in the parms list. */
  prog.AppendParm( new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)),
        DataDirection.InputOutput
  ));
  //Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", new int[]{} );
  prog.Execute();
  //Fetch the returned value.
  CustName = Convert.ToString(
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", 
        new int[]{}));  </pre>
<pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, prog is an initialized As400Program.
  ' We add the field "CustName" to the parm list, and a local
  ' string variable by the same name into it.  After calling the
  ' program, we then set the local variable to the returned
  ' value in the parms list.
  prog.AppendParm( New ProgParm( _
        New ProgParmType("CustName", 0, FieldType.NewChar(40)), _
        DataDirection.InputOutput _
  ))
  ' Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", New Integer(){} )
  prog.Execute()
  ' Fetch the returned value.
  CustName = Convert.ToString( _
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", _
        New Integer(){}))</pre>
<pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here, prog is an initialized As400Program.
   * We add the field "CustName" to the parm list, and a local
   * string variable by the same name into it.  After calling the
   * program, we then set the local variable to the returned
   * value in the parms list. */
  prog.AppendParm( *New ProgParm( +
        *New ProgParmType("CustName", 0, FieldType.NewChar(40)), +
        DataDirection.InputOutput + 
  ))
  //Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", *Nothing *As *Integer4[] )
  prog.Execute()
  //Fetch the returned value.
  CustName = Convert.ToString( +
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", +
        *Nothing *As *Integer4[]))</pre>

## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[As400Program Class](as400program-class.html)
      <br />
[As400Program Class Members](as400program-members.html)
      <br />
[AppendParms Method](as400program-class-append-parms-method.html)
      <br />
[Connection Property](as400program-class-connection-property.html)
      <br />
[ObjectToParm Methods](as400program-class-object-to_parm-method-main.html)
      <br />
[ParmToObject Methods](as400program-class-parm-to_object-method-main.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)
      <br />
[ASNA.DataGate.DataLink.ProgParm Class](prog-parm-class.html)
      <br />
[ASNA.DataGate.DataLink.ProgParmType Class](prog-parm-type-class.html)
      <br />
[ASNA.DataGate.DataLink.StructuredType Class](structure-type-class.html)
      <br />
      [StructuredType Class 
					Constructors](structure-type-class.html)
      <p />

