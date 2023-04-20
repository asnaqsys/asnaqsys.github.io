---
title: QSys Programs and Procedures
---

The Concept of a `Program` in [.NET](https://docs.microsoft.com/en-us/dotnet/core/introduction) is significantly different than that on the IBM i.

.NET is a development platform for building **many kinds** of applications and services.

QSys implements the most important [IBM i Program Semantics](/concepts/background/ibmi-program):

1. Program Activation (and Activation Groups).
2. Keeping Programs Active.
3. Calling Programs and Procedures.

> Note that the term *Module* would be more appropriate when describing a unit of executable instructions on the IBM i, particularly after [ILE Languages](https://www.ibm.com/docs/en/i/7.3?topic=concepts-integrated-language-environment-introduction) were introduced. Strictly speaking, a *Program* (or *Service Program*) is an *IBM i Object* that is made from one or more *Modules*. The *Module* terminology came to the IBM i later, after OPM (*Original Program Model*) was already popular and the community became used to the term *Program* when referring to single-module Object. The term usage: *Calling Programs and Procedures*, is still much more common than the term: *Calling Modules and Procedures*. For this reason, **ASNA Monarch Base** framework uses the word *Program* throughout - when referring to Modules - while naming classes and in the documentation.

The `ASNA.QSys Program` is the class that is used as the *base* class for any `RPG` Migrated Module.

> OPM (*Original Program Model*) RPG Programs are converted to ILE during migration. From now on, when talking about *Programs* we are implying *ILE Programs*.

## Program Activation (and Activation Groups)

Program Activation refers to the runtime process where the object is located (or instanced) and the *named method* is resolved. When talking about *named methods* we are referring to the *implied* Main C-Specs or the *named* Procedure.

> Once a Program is *Activated* the execution of the *named method* is called *Invocation* in ILE terminology.

IBM i jobs were designed to group Program Activations for threading and performance reasons. These groups are called [Activation Groups](https://www.ibm.com/docs/en/i/7.2?topic=i-activation-groups-threads). 

An IBM i RPG Developer can provide directives in the source member to select how *Activations* are grouped. 
Activation Groups are *named*.
ASNA QSys honors naming Activation groups, using class attributes.

For example, the following Program `Custinq` indicates that when *Activated* it should be grouped in the `*DFTACTGRP` group:

```cs
namespace SunFarm.Customers
{
    [ASNA.QSys.HostServices.ActivationGroup("*DFTACTGRP")]
    [ProgramEntry("_ENTRY")]
    public partial class Custinq : ASNA.QSys.HostServices.Program
    {
```

## Keeping Programs Active

After Programs are *Invoked*, and execution of the Procedure completes, the Developer can decide to *end* the activation. To way to indicate that an activation must *end*, the Program sets the [Indicator LR](https://www.ibm.com/docs/en/i/7.4?topic=indicators-last-record-indicator-lr).

When the *Indicator LR* is **not** set, the activation remains in memory.

ASNA QSys uses an `ActivationManager` object to *manage* activations, with methods to:

1. **Get** and instance of a particular Program class. When no instance exists, the `ActivationManager` will create a new one.
2. **Dispose** of an instance when the Program should **not** remain active.

For a detailed step-by-step example of how Activations and Invocations are implemented, please consult [Program Bootstrapping](https://asna.github.io/SunFarm/program-bootstrap/).

## Calling Programs and Procedures

There are two ways to *Invoke* a Program on RPG:

1. CALL (dynamic). The resolution of the Program is delayed until runtime.
2. CALLB (bound).  The resolution of the Program is resolved at compile time.

> The concept of a [Prototype or Procedure Interface](https://www.ibm.com/docs/en/i/7.4?topic=parameters-procedure-interface) is ignored on Migrated code, since
C# compiler will type check **all** bound method parameters.

The implementation of Dynamic and Bound calls are similar, and the C# code you get for a Migration is:

**Migrated CALL example**

```cs
DynamicCaller_.CallD("SunFarm.Customers.ORDHINQ", out _LR, ref ORDCUST);
```

**Migrated CALLB example**
```cs
XamService.MessageSubfileWrite(this, out _, (string)MsgFile, MsgId, MsgDta, MsgLen, 3);
```

## Calling Programs Dynamically

For Dynamic calls the **name of the program is passed as a parameter**, and the *Helper* object instanced on each QSys Program class named DynamicCaller_
will start the *Activation* and *Invocation* process to find and execute the StarEntry method passing the expected parameters.

> Note that the *Activation* rules are defined in the implementation of the **Program**, not in the **CallD**.

The mechanics of **CallD**, and how the runtime locates a called program are described in [CallD](/manuals/programming/programs-and-procedures/call-program.html#CALLD).

For an example using `DynamicCaller_.CallD`, read [Sun Farm Guide](https://asna.github.io/SunFarm/program-bootstrap/)

## Calling *Bound* Procedures

Calling Bound Procedures has some advantages:
1. The compiler makes sure the Program exists in the compiled unit (Project assembly).
2. The compiler can perform type checking on all parameters passed.
3. More than one Procedure can be coded (and properly named) in a Program (or Service Program).
4. When the *caller* is in the same Program, the procedure (class method) can be found very fast.
5. Upon returning from a Procedure (method), the Program **always** remains Active.

Similarities between CallD and Bound Method calls:
1. Both use the QSys `ActivationManager` object.
2. Even when the Bound call looks like a regular C# call to a method, in fact is a call to a **static** method on a class, that may (*or not*) allocate a new instance of the Program class.

The implementation of *Bound* Procedure calls on the QSys Program class, requires more than one C# class method, and the naming of such related names gets tricky:

1. A C# **static** with the **exact** legacy procedure name is implemented (i.e. `public static MessageSubfileWrite`), in the example above.
2. The first parameter of such **static** method is a reference to the caller *self* (or **this**).
3. A **non-static** method with prefix `_` is produced.
4. A **non-static** method with prefix `entry` is produced.

For example, the class `XamService` would have implementations for:

```cs
public static void MessageSubfileWrite(AVRRuntime.ProcedureSupport.ICaller _caller, out Indicator __inLR, FixedString<_10> MsgFile, FixedString<_7> MsgId, FixedString<Len<_1, _0, _0>> MsgDta, int MsgLen, int Level)
{
    // This method is the first reached, and uses ActivationManager to find activation.
}

public void _MessageSubfileWrite(out Indicator __inLR, FixedString<_10> MsgFile, FixedString<_7> MsgId, FixedString<Len<_1, _0, _0>> MsgDta, int MsgLen, int Level)
{
    // This method "guards" the execution of the final procedure, in case call terminates "abruptly".
}

public void entryMessageSubfileWrite(FixedString<_10> MsgFile, FixedString<_7> MsgId, FixedString<Len<_1, _0, _0>> MsgDta, int MsgLen, int Level)
{
    // This is the method where the original legacy code is migrated.
}
```

> Note: The first and second parameters used by the caller are eliminated as it reaches its final **entry** destination.

> Note: When the call to the *Procedure* is done from within the class that defines it, the **static** implementation can short-circuit for performance reasons.

