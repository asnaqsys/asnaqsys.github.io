---
title: As400Program.AppendParms Method

Id: dcsAs400ProgramClassAppendParmsMethod
TocParent: dcsAs400ProgramMethodsMain
TocOrder: 1

keywords: AppendParms method
keywords: As400Program.AppendParms method
keywords: program parameters, append parameter array to
keywords: parameter lists, append parameter array to
keywords: append parameter array to program parameter list
keywords: parameters, append array to program parameter list
keywords: how to, append parameter array to program parameter list

---

Appends an array of parameters to the parameter list for the program. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void AppendParms(
[ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html)[] Parameters
);** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub AppendParms( _
   ByVal Parameters() As [ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html) _
)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AppendParms Acess(*Public)
   DclSrParm Parameters Type([ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html)) Rank(1)** 
      </pre>

## Parameters

<dl>
        <dt>
          <span> *Parameters* 
          </span>
        </dt>
        <dd>
          <span />
 <span style="FONT-FAMILY: Verdana">An array of 
 **ASNA.DataGate.DataLink.ProgParm** </span>
							objects that represents the program parameters to append. </dd>
</dl>

## Exceptions

<span>ArgumentException. A **ProgParm** in the array has the same name as another parameter in the parameter list.</span> 
## Remarks

To create a program parameter list, <span> **ProgParm** </span> objects should be added with the [ AppendParm](as400program-class-append-parm-method.html) or **AppendParms** method in the order of their occurrence in the program parameter list. <span> **AppendParms** </span> appends an array of <span> **ProgParm** </span> objects to the parameter list. The objects are appended sequentially, in the order of their occurrence in the array, such that the first element of the array is appended to the list first.

<span> **ProgParm** </span> objects appended to the list may optionally be named (via the <span> *name* </span> parameter of the [ASNA.DataGate.DataLink.ProgParmType](prog-parm-type-class-prog-parm-type-constructor.html) and [ASNA.DataGate.DataLink.StructuredType](structure-type-class.html) constructors). If a <span> **ProgParm** </span> is named and a previously appended **ProgParm** has the same name, an ArgumentException is raised. 

<span>Note</span> that the parameter list may be constructed with this method before the [ Connection](as400program-class-connection-property.html) property has been set, but the values of the parameters may not be accessed with [ObjectToParm](as400program-class-object-to_parm-method-main.html) and [ParmToObject Method](as400program-class-parm-to_object-method-main.html) until <span> **Connection** </span> has a value.
## Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
      DataDirection.Input)
  };
  prog.AppendParms(Parms);
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  prog.Execute();
  CustName = Convert.ToString(
     prog.ParmToObject(System.Type.GetType("System.String"),
     "CustName",
     new int[]{}));
  TimeOfDay = Convert.ToDecimal(
     prog.ParmToObject(System.Type.GetType("System.Decimal"),
     "TimeOfDay",
     new int[]{}));
              </pre>
<pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, Prog is an initialized As400Program object,
  ' and CustName, TimeOfDay, and Quit400App are valid
  ' string, decimal, and char types respectively.
  Dim Parms As ProgParm()
  Parms = New ProgParm(){ _
     New ProgParm(New ProgParmType("CustName", 0, FieldType.NewChar(40)), _
     DataDirection.Output), _
     New ProgParm(New ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), _
     DataDirection.Output), _
     New ProgParm(New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), _
     DataDirection.Input) _
  }
  prog.AppendParms(Parms)
  prog.ObjectToParm(Quit400App, "Quit400App", New Integer(){})
  prog.Execute()
  CustName = Convert.ToString( _
     prog.ParmToObject(System.Type.GetType("System.String"), _
     "TimeOfDay", _
     New Integer(){}))
  TimeOfDay = Convert.ToDecimal( _
     prog.ParmToObject(System.Type.GetType("System.Decimal"), _
     "TimeOfDay", _
     New Integer(){}))
</pre>
<pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  DclArray Parms Type(ProgParm) Rank(1)
  Parms = *New ProgParm[]{ +
      *New ProgParm(*New ProgParmType("CustName", 0, FieldType.NewChar(40)), +
      DataDirection.Output), +
      *New ProgParm(*New ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), +
      DataDirection.Output), +
      *New ProgParm(*New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), +
      DataDirection.Input) +
  }
  prog.AppendParms(Parms)
  prog.ObjectToParm(Quit400App, "Quit400App", *Nothing *As *Integer4[])
  prog.Execute()
  CustName = Convert.ToString( +
     prog.ParmToObject(System.Type.GetType("System.String"), +
     "CustName", +
     *Nothing *As *Integer4[]))
  TimeOfDay = Convert.ToDecimal( +
     prog.ParmToObject(System.Type.GetType("System.Decimal"), +
     "TimeOfDay", +
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
[AppendParm Method](as400program-class-append-parm-method.html)
      <br />
[Connection Property](as400program-class-connection-property.html)
      <br />
[ObjectToParm Method](as400program-class-object-to_parm-method-main.html)
      <br />
[ParmToObject Method](as400program-class-parm-to_object-method-main.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)
      <br />
[ASNA.DataGate.DataLink.ProgParm Class](prog-parm-class.html)
      <br />
[ASNA.DataGate.DataLink.ProgParmType Class](prog-parm-type-class.html)
      <br />
[ASNA.DataGate.DataLink.StructuredType Class](structure-type-class.html)
      <br />

