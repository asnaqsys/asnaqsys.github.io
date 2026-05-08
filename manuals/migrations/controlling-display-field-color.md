---
title: "Controlling the Color of a Screen Constant or Field"
description: "Master the art of changing display field colors in your UI. This concise guide offers practical tips for dynamic color control."
---

There are multiple ways in which a migrated field or constant can get its color set.  Traditional html/css means can be used for the color selection or one of these two properties of the DdsConstant or DdsXxxField tag-helpers can be employed:
 - Color
 - DisplayAttrCode

## Color Property
The Color property is a [conditional property](/reference/expo/qsys-expo-model/landing-page-namespace.html#conditional-property) string composed of a sets of [conditional values](/reference/expo/qsys-expo-model/landing-page-namespace.html#conditional-value) that evaluates to a Web named color. Conditional values are separated by commas. Each conditional value is composed of a value and an expression which is a combination of indicator values and Boolean operators.

Here are a couple of example that set the color to a fix value without using a full conditional expression features:
```html
    <DdsConstant  Col="10" Text="Customer Number" Color="Green"  />
    <DdsDecField Col="27" For="CUSTREC.SFCUSTNO"  Color="Blue" EditCode="Z" />
```

In this other example, indicators will control the color used to render the field
```html
    <DdsCharField Col="27" For="CUSTREC.SFNAME" 
                  Color="Red : 03 & !99, Green : 06, Blue : 05 | 03, Black:*TRUE"/>
```

The value Red is selected if *IN03 is *ON and *IN99 is *OFF otherwise, the value Green is selected if *IN06 is *ON otherwise, the value Blue is selected if *IN05 or *IN03 are *ON. Finally, if non of the conditions were met, the color selected will be Black.

## DisplayAttrCode Property
Alternatively to using the Color property, it is possible to use a program's field to select the color of a Display Field or Constant. 

The DisplayAttrCode property can reference a field of type byte. The value of the byte field will determine the color.

Here is an usage example, first the tag-helper:
```html
    <div Row="15">
        <DdsConstant Col="12" Text="Company Name:" />
        <DdsCharField Col="27" For="COMPREC.COMPNAME" DisplayAttrCode="@Model.COMPREC.aNAMEATTR"/>
    </div>
    <div Row="16">
        <DdsConstant Col="12" Text="Contact Name:" />
        <DdsCharField Col="27" For="COMPREC.CONTACT" DisplayAttrCode="@Model.CUSTREC.aCONTACT"/>
    </div>

```
And then the model:
```cs
public class COMPREC_Model : RecordModel
{
    . . . 
    [Byte(Alias = "@NAMEATTR")]
    public byte aNAMEATTR { get; private set; } // Color Attr: Name

    [Byte(Alias = "@CONTACT")]
    public byte aCONTACT { get; private set; } // Color Attr: Contact

    [Char(40, ProtectCodeFieldName = nameof(aNAMEATTR))]
    public string COMPNAME { get; set; }

    [Char(40)]
    public string CONTACT { get; set; }
   
    . . .
```
### Bit Usage

The character field COMPNAME from record COMPREC will be display at column 27 with a color according to the value of the field aNAMEATTR. The field being display (COMPNAME) and the one with the display attribute (aNAMEATTR) are typically defined in the same record (COMPREC) as both are used on the same output operation.

The bits in the value of the attribute field are used to control the display attributes as follows (bit 0 is the least significant bit):

| Bit     | Usage          | Legacy use on IBM i | Notes
| ------- | -------------- | ------------------- | -----
| 0       | Reverse Image  | Reverse Image       | If bit=1, Swap Foreground Color with Background Color
| 1       | Select Color   | High Intensity      | 
| 2       | Underline      | Underline           | If bit=1, Underline the field
| 3       | Select Color   | Blink               | 
| 4       | Select Color   | Column Separator    | 
| 5       |                |                     | Should always be set to '1'
| 6       |                |                     | Should always be set to '0'
| 7       | Unused         |                     | 
| 8       | Protect        | Protect             | If bit=1, Protects the field from input

### Actual Color

The actual color is govern by bits 1, 3 and 4 as follows:

| Bit 1 | Bit 3 | Bit 4 | Color
| ------| ----- | ----- | -----
| 0     |     0 |     0 | Green
| 0     |     0 |     1 | DarkBlue
| 0     |     1 |     0 | Red
| 0     |     1 |     1 | Red
| 1     |     0 |     0 | DarkTurquoise
| 1     |     0 |     1 | DarkBlue
| 1     |     1 |     0 | DeepPink
| 1     |     1 |     1 | Blue

### Protecting a Field

If a field is to be protected via a display attribute byte, it is necessary to add the name of the protecting field in the type attribute for the protected field in its definition on the model.  If the field COMPNAME is to be protected via the value of Bit 8 of field aNAMEATTR, then define COMPNAME as this: 

```cs
    [Char(40, ProtectCodeFieldName = nameof(aNAMEATTR))]
    public string COMPNAME { get; set; }
```



