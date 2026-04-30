---
title: "SingleRecordProgram class"
description: "Represents the SingleRecordProgram type in ASNA.QSys.EscapeFX."
---

Represents the SingleRecordProgram type in ASNA.QSys.EscapeFX.

**Namespace:** ASNA.QSys.EscapeFX
**Assembly:** ASNA.QSys.EscapeFX.dll

**Inheritance:** InteractiveProgram

The SingleRecordProgram serves as the base class for programs that Edit or Display one record at a time.  The program can have one, two or three screens.

## Constructors

| Name | Description |
| --- | --- |
| SingleRecordProgram() | Initializes a new instance of the SingleRecordProgram class. |


## Fields

| Type | Name | Description | Previous Name (PKA in Synon) |
| --- | --- | --- | --- |
| int | MaximumScreenKinds | Maximum number of detail screen kinds. |  |
| FixedString<_1> | RepeatDisplay | Repeat-display flag state. | W0RPT |
| FixedString<_1> | RollFlag | Roll/page navigation flag state. | W0ROL |
| int | Screen1IndicatorCount | Number of indicators tracked for detail screen 1. |  |
| char[] | Screen1Indicators | Indicator snapshot for detail screen 1. |  |
| int | Screen2IndicatorCount | Number of indicators tracked for detail screen 2. |  |
| char[] | Screen2Indicators | Indicator snapshot for detail screen 2. |  |
| int | Screen3IndicatorCount | Number of indicators tracked for detail screen 3. |  |
| char[] | Screen3Indicators | Indicator snapshot for detail screen 3. |  |
| FixedDecimal<_3, _0> | ScreenKind | Active detail screen kind. | W0SCR |

## Indicator Properties

In addition to generic `inXX` properties inherited from the base classes of EscapeProgram and InteractiveProgram, this SingeRecordProgram class provides indicator 11 with a significant name indicating a request to delete.

| Type | Name | Description |
| --- | --- | --- |
| bool | inF11Delete | Gets or sets the value of _IN[11] which reflects the user having pressed the F11 Function Key,  signaling a Delete operation. |

## Methods

| Signature | Description |
| --- | --- |
| [CheckParms](single-record-program-check-parms.html#void-checkparms)() | CheckParms operation. |
| [ClearScreen1Indicators](single-record-program-clear-screen1-indicators.html#void-clearscreen1indicators)() | ClearScreen1Indicators operation. |
| [ClearScreen2Indicators](single-record-program-clear-screen2-indicators.html#void-clearscreen2indicators)() | ClearScreen2Indicators operation. |
| [ClearScreen3Indicators](single-record-program-clear-screen3-indicators.html#void-clearscreen3indicators)() | ClearScreen3Indicators operation. |
| [ClearScreenIndicators](single-record-program-clear-screen-indicators.html#void-clearscreenindicators)() | ClearScreenIndicators operation. |
| [clearScreenIndicators](single-record-program-clear-screen-indicators.html#void-clearscreenindicatorschararrayint)(char [] screenIndicators, int screenIndicatorCount) | clearScreenIndicators operation. |
| [ConvertKeyToExternal](single-record-program-convert-key-to-external.html#void-convertkeytoexternal)() | ConvertKeyToExternal operation. |
| [DisplayNextScreen](single-record-program-display-next-screen.html#void-displaynextscreen)() | Display next screen |
| [DisplayPreviousScreen](single-record-program-display-previous-screen.html#void-displaypreviousscreen)() | Display previous screen |
| [DisplayScreen](single-record-program-display-screen.html#void-displayscreen)() | Display and process detail screen |
| [errorsInScreen](single-record-program-errors-in-screen.html#bool-errorsinscreenchararrayint)(char[] screenIndicators, int screenIndicatorCount) | errorsInScreen operation. |
| [ErrorsInScreen](single-record-program-errors-in-screen.html#bool-errorsinscreenint)(int screenNumber) | ErrorsInScreen operation. |
| [InitKeyScreenFields](single-record-program-init-key-screen-fields.html#void-initkeyscreenfields)() | InitKeyScreenFields operation. |
| [InitProgram](single-record-program-init-program.html#void-initprogram)() | InitProgram operation. |
| [IsAnyKeyFieldBlank](single-record-program-is-any-key-field-blank.html#bool-isanykeyfieldblank)() | IsAnyKeyFieldBlank operation. |
| [ProcessHome](single-record-program-process-home.html#void-processhome)() | ProcessHome operation. |
| [ProcessKeyScreen](single-record-program-process-key-screen.html#void-processkeyscreen)() | ProcessKeyScreen operation. |
| [ProcessRecord](single-record-program-process-record.html#void-processrecord)() | ProcessRecord operation. |
| [ProgramMainLoop](single-record-program-program-main-loop.html#void-programmainloop)() | ProgramMainLoop operation. |
| [RedisplayPreviousScreen](single-record-program-redisplay-previous-screen.html#void-redisplaypreviousscreen)() | Redisplay previous screen |
| [ResetScreenFields](single-record-program-reset-screen-fields.html#void-resetscreenfields)() | ResetScreenFields operation. |
| [SetCursor1](single-record-program-set-cursor1.html#void-setcursor1)() | SetCursor1 operation. |
| [SetCursor2](single-record-program-set-cursor2.html#void-setcursor2)() | SetCursor2 operation. |
| [SetCursor3](single-record-program-set-cursor3.html#void-setcursor3)() | SetCursor3 operation. |
| [SetDisplayAttributes](single-record-program-set-display-attributes.html#void-setdisplayattributes)() | Set detail screen conditioning indicators |
| [SetDisplayKeyAttributes](single-record-program-set-display-key-attributes.html#void-setdisplaykeyattributes)() | Set key screen conditioning indicators |
| [ShowKeyScreen](single-record-program-show-key-screen.html#void-showkeyscreen)() | Display key screen and process HELP requests |
| [ShowScreen](single-record-program-show-screen.html#void-showscreen)() | Display screen and process HELP requests |
| [ValidateDetails](single-record-program-validate-details.html#void-validatedetails)() | ValidateDetails operation. |
| [ValidateRecord](single-record-program-validate-record.html#void-validaterecord)() | Validate record |

## See Also
- [InteractiveProgram](interactive-program.html)
- [DisplayRecordFunction](display-record-function.html)
- [EditRecordFunction](edit-record-function.html)
