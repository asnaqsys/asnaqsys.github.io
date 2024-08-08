---
title: "FieldAttribute class          | QSYS API Reference Guide"
description: "Provides Displayfile field attributes "
last_modified_at: 2024-08-08T21:42:10Z
---

Provides Displayfile field attributes

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Remarks

IBM i Displayfiles allows the designer to specify metadata (via keywords) on fields that describe how fields should interact with user. For example, [DDS](https://www.ibm.com/docs/en/i/7.1?topic=ddf-dds-keyword-entries-display-files-positions-45-through-80) allows th indicate that a particular field on a records should be [protected](https://www.ibm.com/docs/en/i/7.1?topic=80-dspatr-display-attribute-keyword-display-files) from input, conditioned to a particular option indicator. 

For example, the following DDS specifications define field `SITMNBR` (in Record format `ORDLINE`), where not only does it describe the type and length of the display field, but the fact that when Indicator 88 is `On`, the field should be protected from input (aka read-only).

```
0076.00     A            SITMNBR        9Y 0B  3 15                                    000000
0078.00     A  88                                  DSPATR(PR)                          000000
```

Razor syntax nor HTML syntax use the concept of Indicators. Fields in Expo may include attributes, such as `Protect` (indicated below), that complete the specification.

```cs
public class ORDLINE_Model : RecordModel
{
    .
    .
    .

    [Dec(9, 0, Protect = "88")]
    public decimal SITMNBR { get; set; }

   .
   .
   .
}
```

The name indicated in C# syntax for the Field Attributes maps to the Properties listed on this class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Alias | Field Alias name |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | BlanksIndicator | Blanks indicator |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ChangeIndicator | Change indicator |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | OutputData | Output Data |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Protect | Protect indicator |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ProtectCodeFieldName | Protect Code field name |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#fieldattribute-getfrommemberinfo-fieldmember)([MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0)) | Gets a FieldAttribute from the given MemberInfo

### FieldAttribute GetFrom([MemberInfo fieldMember](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0))

Gets a FieldAttribute from the given MemberInfo

```cs
FieldAttribute GetFrom(MemberInfo fieldMember)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [MemberInfo](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.memberinfo?view=net-8.0) | fieldMember | Field member information

#### Returns

| Type | Description
| --- | ---
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | the field attribute
