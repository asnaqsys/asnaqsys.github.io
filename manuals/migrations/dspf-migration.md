---
title: "Migration of Display Files"
description: "Master Display-File migration with our guide. Learn key strategies, tips for smooth transition, and how to avoid common pitfalls in the process."
---

## Display Files

Display files are migrated into Razor Pages.  The migration strategy for each display file is to create a Razor Page composed of two files.  First, there is an `.cshtml` file containing HTML and Tag Helpers describing the layout and rendering (view) composition of the display.

Second, an `.cshtml.cs` file contains the data model describing the type of each field in each record format. The model extends the Monarch class ASNA.QSys.Expo.Model.DisplayPageModel which provides the interchange of data with the program using the display file.

The Monarch Display File Agent creates the Razor Page taking as input the OS/400 display files DDS specifications.  Most of the elements found in the DDS specification are migrated. However, there are two general features which today are not dealt with: Help and window widgets. There are multiple keywords that form these two groups.  The help system defined in the DDS is alien to the web model and it is not migrated. With regards to window widgets, in the mid 90s, DDS incorporated a set of keywords to facilitate the creation of Windows-looking screens.  Because specialized hardware was needed to render these keywords properly, the practice of using them never caught on.  The exception is the support for the WINDOW keyword which is supported by Monarch as a kind of pop-up window in the browser.

Monarch provides modern user interface elements such as calendar controls, drop-down lists, button images that can be easily used to replace window widget DDS types.

### HTML `class` may be get augmented

If a field is found to be 'in error', due to bad user input (e.g. number out of range) or because the application turned `on` an error indicator for the field, Monarch appends to the HTML class attribute the style `dds-field-in-error`.
 
The style `dds-field-in-error` is defined in the website's *wwwroot/lib/asna-expo/css/expo.css* as:
 
```css
.dds-field-in-error {
    color: red;
}
```
 
The style can be redefined by overriding it in *wwwroot/css/site.css*.

Similarly, right-alignment for decimal fields is done by appending the class `dds-dec-field-alignment`.

## DDS Display File Keywords

The following tables specify the level of support provided by Monarch for Display file DDS keywords.

### Display Field-Level Keywords

| **Supported** | **May be supported in future release** | **Not applicable** |**Unsupported** |
| --- | --- | --- | --- |
| AID | CHGINPDFT | AUTO | CHRID |
| ALIAS | CHKMSGID | BLKFOLD | DUP |
| BLANKS | DLTCHK | CMP | EDTMSK |
| CHANGE | DLTEDT | OVRATR | ENTFLDATR |
| CHECK | DFTVAL | OVRDTA | NOCCSID |
| COLOR | FLDCSRPRG | PUTRETAIN | |
| COMP | FLTFIXDEC | WRDWRAP | |
| CNTFLD | FLTPCN | | |
| DATE | HTML | |   |
| DATFMT | INDTXT | |   |
| DATSEP | MAPVAL | |   |
| DFT | VALNUM |   |   |
| DSPATR [^1] | |   |   |
| EDTCDE | |   |   |
| EDTWRD | |   |   |
| ERRMSG | |   |   |
| ERRMSGID | |   |   |
| LOWER |   |   |   |
| MSGCON | | | |
| MSGID |   |   |   |
| RANGE |   |   |   |
| REFFLD |   |   |   |
| SYSNAME |   |   |   |
| TEXT |   |   |   |
| TIME |   |   |   |
| TIMFMT |   |   |   |
| TIMSEP |   |   |   |
| USER |   |   |   |
| VALUES |   |   |   |

### Display Record-Level Keywords

| **Supported** | **May be supported in future release** | **Not applicable** | **Unsupported** |
| --- | --- | --- | --- |
| ALTNAME | CHGINPDFT | OVRATR | ALARM |
| CAnn | CLRL | OVRDTA | ALWGPH |
| CFnn | HELP | PUTOVR | ALWROL |
| CHANGE | INDTXT | PUTRETAIN | ASSUME |
| CHECK | LOGINP | RMVWDW | BLINK |
| CSRLOC | LOGOUT | WDWBORDER | CCSID |
| ERASE | VALNUM | WRDWRAP | CLEAR |
| OVERLAY | |   | CSRINPUT |
| PAGEDOWN |   |   | CSRINPONLY |
| PAGEUP |   |   | DSPMOD |
| PRINT |   |   | ENTFLDATR |
| PROTECT |   |   | ERASEINP |
| RTNCSRLOC [^2] |   |   | FRCDTA |
| RTNDTA |   |   | GETRETAIN |
| ROLLDOWN |   |   | HOME |
| ROLLUP |   |   | INVITE |
| SETOF(F) |   |   | INZINP |
| SLNO [^3] |   |   | INZRCD |
| TEXT |   |   | KEEP |
| VLDCMDKEY |   |   | LOCK |
| WDWTITLE |   |   | MDTOFF |
| WINDOW |   |   | MSGALARM |
|   |   |   | RETCMDKEY |
|   |   |   | RETKEY |
|   |   |   | RETLCKSTS |
|   |   |   | UNLOCK |
|   |   |   | USRDFN |

### Display File-Level Keywords

| **Supported** | **May be supported in future release** | **Not applicable** | **Unsupported** |
| --- | --- | --- | --- |
| CAnn | ALTHELP | INDARA | ALTPAGEDWN |
| CFnn | CHGINPDFT | WRDWRAP | ALTPAGEUP |
| CHECK | DSPRL |   | ALWGPH |
| ERRSFL | HELP |   | CLEAR |
| PAGEDOWN | INDTXT |   | CSRINPONLY |
| PAGEUP | MSGLOC |   | DSPSIZ |
| PRINT | VALNUM |   | ENTFLDATR |
| REF |   |   | HOME |
| ROLLDOWN |   |   | INVITE |
| ROLLUP |   |   | MSGALARM |
| VLDCMDKEY |   |   | OPENPRT |
| WDWBORDER |   |   | PASSRCD |
|   |   |   | PRINT(Lib/File) |
|   |   |   | USRDSPMGT |


### Subfile Keywords

| **Supported** | **May be supported in future release** | **Unsupported** |
| --- | --- | --- |
| SFL | SFLINZ | SFLCSRPRG |
| SFLCLR | SFLRNA | SFLDLT |
| SFLCTL | | SFLENTER |
| SFLCSRRRN | | SFLROLVAL |
| SFLDROP | | SFLSCROLL |
| SFLDSP |  | |
| SFLDSPCTL | | |
| SFLEND | | |
| SFLFOLD | | |
| SFLLIN | | |
| SFLMODE |   | |
| SFLMSG |   | |
| SFLMSGID |   |   |
| SFLMSGKEY |   |   |
| SFLRCDNBR |   |   |
| SFLSMGRCD |   |   |
| SFLNXTCHG |   |   |
| SFLPAG |   |   |
| SFLPGMQ |   |   |
| SFLSIZ |   |   |

### Display Attributes for DSPATR Keyword

| **Supported** | **May be supported in future release** | **Unsupported** |
| --- | --- | --- |
| ND-Non Display | HI-High Intensity | BL-Blinking Field |
| PC-Position Cursor | | CS-Column Separator |
| PR-Protect |   | MDT-Set Change Data Tag |
|   |   | OID-Operator Identification |
|   |   | SP-Select by Light Pen |
|   |   | RI-Reverse Image |
|   |   | UL-Underline |


----

[^1]: See [supported Display Attributes](#display-attributes-for-dspatr-keyword)

[^2]: Support is not provided for cursor positioning **within** a field.

[^3]: Support is not provided for (\*VAR)

