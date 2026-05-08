---
title: "User Defined Command translated to a CALL to Execute method on new Class."
description: "Describes one of the alternatives to translate User Defined commands (calling a class method)."
---

The migrator provides a new class that has properties for all possible parameters the User Defined command may have.

The class is instanced in code, the available properties are loaded from provided fields or values.

A call to an `Execute` method is made.

>Using this target type produces less migration lines, particularly for User Defined commands with lots of possible parameters, and the usage may only include a few.


<br>

## Command Element Node (valid attributes)

| Attribute | Description | Default value |
| --- | --- | --- |   
| name          | The name of the user defined command in the legacy source code that is being redefined. | (Required) |
| class_name    | Name of the class implementing the Command.<br/> The Class should implement an `Execute` function - or method in C# terminology.<br/> May be fully qualified. | (Required) |


<br>

## Parameter Element Node (valid attributes)

| Attribute | Description | Notes |
| --- | --- | --- |   
| keyword         | The name of the keyword in the legacy source code that is being defined. | (Required)
| data_type       | The type of parameter. (See [Advanced parameter data-types](/manuals/cocoon/cl-user-def-schema.html#advanced-parameter-data-types)). |
| data_len        | The length of parameter. |
| prop_name       | The name of the property to receive the parameter | (Required)
| by              | How the parameter is passed, "value" or "reference" | Defaults to "value" 
| element_list    | Contains a list of elements. |
| legacy_values   | The list of possible values that the parameter may contain, which will be replaced by the corresponding migrate_values.
| migrate_values  | The list of enumeration or constant values that will replace the corresponding legacy_values. For example, if legacy_values contained "*ADD, *REPL, *DEL" the corresponding values in migrate_values could be "enum.ADD, enum.REPLACE, enum.DELETE" to indicate the enumeration values to replace the legacy_values. |
| required        | Indicates if the parameter is required (*Yes) or not (*No). |
| default_value   | Default value of the parameter. |
| constructor_parm | Indicates if this is a constructor parameter (*True). When used, prop_name is invalid and by must be "reference". |

<br>

## Example 1: CL User defined Command calls Execute on a new class.

Let's assume we have a CL Program named **ExampleCL** that is using the User-defined command "IPMOVDTA" command:


```
0001.00             PGM                                                                040826
0002.00                                                                                040826
0003.00             IPMOVDTA   FROMFILE('CUSTOMER') +                                  040826
0004.00                        FROMMBR('SALES')     +                                  040826
0005.00                        TOMBR('RETURNS')                                        040826
0006.00             RETURN                                                             040826
0007.00                                                                                040826
0008.00             ENDPGM                                                             040826
```

We could encapsulate the new implementation in a class called `IPMoveFileData`, where we define properties for each of the parameters.

```cs
DclNamespace ACME.Utilities

Using System
Using ASNA.QSys.Runtime
Using ASNA.QSys.Runtime.JobSupport

BegClass IPMoveFileData Access(*Public)

    DclFld FromFile Access(*Public) Type(*String)
    DclFld FromMember Access(*Public) Type(*String)
    DclFld ToMember Access(*Public) Type(*String)

    BegSr Execute Access(*Public)
        // Logic to Move member from FromFile/FromMember to ToMember
    EndSr
EndClass
```

The *CL User Defined Commands* Dictionary may be defined as the following:

```xml
<?xml version="1.0" encoding="utf-8"?>
<ClassTemplate>
   <command name="IPMOVDTA" class_name="ACME.Utilities.IPMoveFileData">
      <parameter keyword="FROMFILE" prop_name="FromFile" data_type="*String" data_len="10"/>
      <parameter keyword="FROMMBR" prop_name="FromMember" data_type="*String" data_len="10"/>
      <parameter keyword="TOMBR" prop_name="ToMember" data_type="*String" data_Len="10"/>
   </command>
</ClassTemplate>
```
<br>

When Migrating, the following code would be produced:

```cs
BegClass ExampleCL Extends(CLProgram) Access(*Public)


//------------------------------------------------------------------------------ 
//  "*Entry" Mainline Code (Monarch generated)
//------------------------------------------------------------------------------ 
    BegProc *Entry Access( *Public )

        *INLR = *ON

        DclFld cmdIPMOVDTA Type(ACME.Utilities.IPMoveFileData) New()
        
        cmdIPMOVDTA.FromFile   = "CUSTOMER"
        cmdIPMOVDTA.FromMember = "SALES"
        cmdIPMOVDTA.ToMember   = "RETURNS"
        
        cmdIPMOVDTA.Execute()
        Return


    EndProc

EndClass
```

>Note: IPMoveFileData is a .NET class that defines a type. Field `cmdIPMOVDTA` of Type `ACME.Utilities.IPMoveFileData` news to be instanced (via keyword `New`) to be created. Properties are loaded using the command parameters and finally, the implementation logic runs in the `Execute` subroutine.
