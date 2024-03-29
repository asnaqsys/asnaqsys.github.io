---
title: CallerActivationGroupAttribute Class

---

The <code> **CallerActivationGroupAttribute** </code> is provided to support the job activation manager when a program is to be allocated in the same activation group as the program by which it is called.

For a list of all members of this class, see [Class Members](caller-activation-group-attribute-class-members.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](monarch-namespace.html)
 **ASNA.Monarch.CallerActivationGroupAttribute**   </pre>

#### Syntax
<pre class="syntax"> **Public class CallerActivationGroupAttribute Inherits System.Attribute** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
The **Job** maintains an ***activation manager*** responsible for handling the activations of programs according to the ActivationGroup custom attribute defined in the <code> **BegClass** </code> of the program. The following code examples shows a program (<code>Custcalc</code>) that is to be allocated in the same activation group as the program calling this program.
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes ( CallerActivationGroup ())</pre>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](monarch-namespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dt>
        [ASNA.Monarch
      Namespace](monarch-namespace.html)</dt><dt>
        [
      CallerActivationGroupAttribute Class Members](caller-activation-group-attribute-class-members.html) 
     </dt><dt>[
      ActivationGroupAttribute Class](activation-group-attribute-class.html)</dt><dt>[
      NewActivationGroupAttribute Class](new-activation-group-attribute-class.html)</dt></dl>

