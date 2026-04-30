---
title: "InteractiveProgram Class"
description: "Abstract base class for user-interactive programs in ASNA.QSys.EscapeFX."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** [EscapeProgram](escape-program.html)

Abstract base class extending `EscapeProgram` for screen-based interactive applications. Provides workstation file integration, prompting, cursor management, window positioning, and field validation.

## Constructors

| Signature | Description |
| --- | --- |
| `InteractiveProgram()` | Initializes a new instance of the InteractiveProgram class. |

## Fields

| Type | Name | Description | Previous Name (PKA in Synon) |
| --- | --- | --- | --- |
| FixedString<_1> | BypassFirstScreen | Bypass-first-screen flag state. | W0BYP |
| FixedString<_40> | CompanyName | Company name text. | ##CMP |
| FixedString<_40> | ConfirmOperation | Confirmation response value. | ##CFCD - ZZCFCD |
| FixedDecimal<_5, _0> | CursorCol | Cursor column position. | W0CCL |
| FixedString<_10> | CursorFieldName | Cursor field identifier. | W0CFL |
| FixedString<_3> | CursorLocationFlag | Cursor location control flag. | WCSRLC |
| FixedDecimal<_5, _0> | CursorRow | Cursor row position. | W0CRW |
| FixedDecimal<_5, _0> | CursorRowCol | Combined cursor row/column value. | ZINPOS |
| FixedString<_1> | DeferConfirmation | Defer-confirmation flag state. | W0DCF |
| FixedString<_1> | GroupLabel | Group label value. | W0GRP |
| FixedDecimal<_5, _0> | HelpColumn | Help cursor column value. | YYCL |
| FixedString<_10> | HelpLabel | Help label value. | YYHLVN |
| FixedDecimal<_5, _0> | HelpLabelGroupCount | Count of help label groups. | YYLGC |
| FixedDecimal<_5, _0> | HelpLabelGroupCountT | Temporary help label group count. |  |
| FixedString<_10> | HelpLabelGroups | Help label group identifiers. | YYLGVN |
| FixedString<_10> | HelpOptions | Help options value. | YYUSOP |
| FixedDecimal<_5, _0> | HelpPromptCursorCol | Prompt cursor column for help. | ZHCSCL |
| FixedDecimal<_5, _0> | HelpPromptCursorRow | Prompt cursor row for help. | ZHCSRW |
| FixedDecimal<_4, _0> | HelpPromptRow | Help prompt row value. | ZHF4RW |
| FixedDecimal<_3, _0> | HelpPromptSavedCol | Saved prompt cursor column. | ZZCSCL |
| FixedDecimal<_3, _0> | HelpPromptSavedRow | Saved prompt cursor row. | ZZCSRW |
| FixedDecimal<_5, _0> | HelpRow | Help cursor row value. | YYRW |
| FixedString<_10> | HelpTextFile | Help text file name. | YYHPFL |
| FixedString<_10> | HelpTextLibrary | Help text library name. | YYHPLB |
| FixedString<_10> | HelpTextSource | Help text source member name. | W0HPMB |
| FixedString<_1> | IsTransaction | Transaction mode flag state. | W0TRN |
| FixedString<_1> | LocateAction | Locate action mode value. | YWLCTP |
| FixedString<_1> | NameSearchRequired | Name-search-required flag state. | W0NSRQ |
| FixedDecimal<_3, _0> | NextCursorCol | Next cursor column value. | W0COL0 |
| FixedDecimal<_3, _0> | NextCursorRow | Next cursor row value. | W0ROW0 |
| FixedString<_1> | NullRecord | Null-record indicator value. | W0NLR |
| readonly FixedString<_30> | Off30Indicators | Precomputed off-state indicator string. | ##OFF |
| FixedString<_10> | OverrideCursor | Cursor override value. | W0OVR0 |
| FixedDecimal<_1, _0> | PanelNumber | Active panel number. | YWPNNO |
| FixedString<_3> | ProgramMode | Program mode code. | W0PMD |
| bool | PromptConfirmationInitialValue | Initial default for confirmation prompts. |  |
| FixedString<_10> | PromptedFieldName | Name of currently prompted field. | YPMTFD |
| FixedString<_1> | RereadSubfileRecord | Reread-subfile-record flag state. | W0SNC |
| FixedString<_1> | RequestHelp | Help-request flag state. | W0HLP |
| bool | RequiresConfirmation | Indicates whether confirmation is required. |  |
| FixedString<_1> | RetrievalFunction | Retrieval function code. | YWRTFN |
| FixedDecimal<_6, _0> | ScreenTime | Screen timestamp value. | ##TME or ZZTME |
| FixedString<_1> | SetCursor | Set-cursor flag state. | YSETCS |
| bool | UsesWindows | Indicates whether window behavior is enabled. |  |
| FixedDecimal<_3, _0> | WindowCol | Window column position. | YWWDCL |
| FixedDecimal<_3, _0> | WindowDepth | Window depth value. | YWWDDP |
| int[] | WindowDepths | Window depths per panel. |  |
| FixedStringArray<_4, _1> | WindowLocationAllowed | Window-location-allowed flags by panel. | YSL |
| FixedDecimal<_3, _0> | WindowPromptCol | Window prompt start column. | YWPOC1 |
| FixedDecimal<_3, _0> | WindowPromptColEnd | Window prompt end column. | YWPOC2 |
| FixedDecimal<_3, _0> | WindowPromptRow | Window prompt row. | YWPORW |
| FixedDecimal<_3, _0> | WindowRow | Window row position. | YWWDRW |
| FixedDecimal<_3, _0> | WindowStart1Col | Window 1 start column. | ##WSC1 or ZZWSC1 |
| FixedDecimal<_3, _0> | WindowStart1Row | Window 1 start row. | ##WSR1 or ZZWSR1 |
| FixedDecimal<_3, _0> | WindowStart2Col | Window 2 start column. | ##WSC2 or ZZWSC2 |
| FixedDecimal<_3, _0> | WindowStart2Row | Window 2 start row. | ##WSR2 or ZZWSR2 |
| FixedDecimal<_3, _0> | WindowStart3Col | Window 3 start column. | ##WSC3 or ZZWSC3 |
| FixedDecimal<_3, _0> | WindowStart3Row | Window 3 start row. | ##WSR3 or ZZWSR3 |
| FixedDecimal<_3, _0> | WindowStartCol | Window start column. | ##WSC or ZZWSC |
| int[] | WindowStartCols | Window start columns per panel. |  |
| FixedDecimal<_3, _0> | WindowStartRow | Window start row. | ##WSR or ZZWSR |
| int[] | WindowStartRows | Window start rows per panel. |  |
| FixedDecimal<_3, _0> | WindowWidth | Window width value. | YWWDWD |
| int[] | WindowWidths | Window widths per panel. |  |


## Properties

| Signature | Description | Previous Name (PKA in Synon) |
| --- | --- |
| `abstract WorkstationFileBase MainWorkstationFile { get; }` | Gets the main workstation file for the program. |
| `bool CancelRequested { get; set; }` | Gets or sets whether a cancel operation has been requested. |
| `bool RefreshScreenRequested { get; set; }` | Gets or sets whether a screen refresh has been requested. |
| `string ProgramMode { get; set; }` | Gets or sets the current program mode (e.g., `"ADD"`, `"CHG"`). |
| `string BypassFirstScreen { get; set; }` | Gets or sets whether the first screen should be bypassed. |
| `string IsTransaction { get; set; }` | Gets or sets whether the program is in a transaction state. |
| `string SetCursor { get; set; }` | Gets or sets the cursor control flag. |
| `string WorkstationFormatPrefix { get; }` | Gets the format prefix for the workstation file. |
| `FixedString<_10> ScreenFormat { get; }` | Gets the ScreenFormat value. | @#DFMT |
| `short ScreenLowestSubfile { get; }` | Gets the Screen Lowest Subfile Record value. |  @#SFRC |
| `short ScreenRowCol { get; }` | Gets the Screen RowCol value. | @#RWCL |
| `short ScreenWindowRowCol { get; }` | Gets the Window RowCol value. | @#WWRC |

## Indicator Properties

In addition to generic `inXX` properties inherited from the base class EscapeProgram, this InteractiveProgram class provides properties with significant names for the first 30 indicators which are used to identify which function key was pressed by the user, and other screen related flags.

| Type | Name           | Description |
| --- | --------------- | --- |
| bool | inF01          | Gets or sets the fact that the User pressed the F01 Function Key |
| bool | inF02          | Gets or sets the fact that the User pressed the F02 Function Key |
| bool | inF03Exit      | Gets or sets the fact that the User pressed the F03 Function Key |
| bool | inF04Prompt    | Gets or sets the fact that the User pressed the F04 Function Key |
| bool | inF05          | Gets or sets the fact that the User pressed the F05 Function Key |
| bool | inF06          | Gets or sets the fact that the User pressed the F06 Function Key |
| bool | inF07          | Gets or sets the fact that the User pressed the F07 Function Key |
| bool | inF08          | Gets or sets the fact that the User pressed the F08 Function Key |
| bool | inF09ChangeMode | Gets or sets the fact that the User pressed the F09 Function Key |
| bool | inF10          | Gets or sets the fact that the User pressed the F10 Function Key |
| bool | inF11          | Gets or sets the fact that the User pressed the F11 Function Key |
| bool | inF12          | Gets or sets the fact that the User pressed the F12 Function Key |
| bool | inF13          | Gets or sets the fact that the User pressed the F13 Function Key |
| bool | inF14          | Gets or sets the fact that the User pressed the F14 Function Key |
| bool | inF15          | Gets or sets the fact that the User pressed the F15 Function Key |
| bool | inF16          | Gets or sets the fact that the User pressed the F16 Function Key |
| bool | inF17          | Gets or sets the fact that the User pressed the F17 Function Key |
| bool | inF18          | Gets or sets the fact that the User pressed the F18 Function Key |
| bool | inF19          | Gets or sets the fact that the User pressed the F19 Function Key |
| bool | inF20          | Gets or sets the fact that the User pressed the F20 Function Key |
| bool | inF21          | Gets or sets the fact that the User pressed the F21 Function Key |
| bool | inF22          | Gets or sets the fact that the User pressed the F22 Function Key |
| bool | inF23          | Gets or sets the fact that the User pressed the F23 Function Key |
| bool | inF24          | Gets or sets the fact that the User pressed the F24 Function Key |
| bool | in25Help       | Gets or sets the fact that the User pressed the Help Key |
| bool | in26Clear      | Gets or sets the fact that the User pressed the Clear Key |
| bool | in27PageDown   | Gets or sets the fact that the User pressed the PageDown Key |
| bool | in28PageUp     | Gets or sets the fact that the User pressed the PageUp Key |
| bool | in29NotEnter   | Gets or sets the fact that the User *did not* pressed the Enter Key |
| bool | in30Home       | Gets or sets the fact that the User pressed the Home Key |
| bool | in86PutOverrides | Gets or  sets the request to Put Overrides which has no bearing on .NET |
| bool | in87ProtectOtherFields | Gets or  sets the request to Protect the other fields |
| bool | in88ProtectMainFields | Gets or  sets the request to Protect the Main Fields |
| bool | in89AddMode    | Gets or sets the Add Mode  |
| bool | in93LargeDisplay | Gets or sets the indicator that Large Displays are being used |
| bool | in94SetCursor  | Gets or  sets the request to Set the Cursor |
| bool | in96BadConfirm | Gets or sets the flag indicating a Bad Confirm|
| bool | in98ForceInput | Gets or sets the request to Force Input value. |


## Methods

| Signature | Description |
| --- | --- |
| [override void InitProgram()](interactive-program-init-program.html) | Initializes interactive-specific fields and workstation setup. |
| [virtual void ConvertToExternal()](interactive-program-convert-to-external.html) | Converts internal fields to external display form. |
| [virtual void ShowScreen()](interactive-program-show-screen.html) | Displays the current screen. |
| [virtual void CancelProgram()](interactive-program-cancel-program.html) | Handles program cancellation. |
| [virtual void ProcessPrompt()](interactive-program-process-prompt.html) | Processes a prompt request from the user. |
| [virtual void DisplayHelp()](interactive-program-display-help.html) | Displays context-sensitive help. |
| [virtual void ProcessNamePrompt()](interactive-program-process-name-prompt.html) | Processes a name-field prompt. |
| [void SetCursor0()](interactive-program-set-cursor0.html) | Positions the cursor at the default location. |
| [void TestCursor()](interactive-program-test-cursor.html) | Tests and adjusts the cursor position. |
| [void ClearCursor()](interactive-program-clear-cursor.html) | Clears the cursor positioning flags. |
| [void SetCursorInField(string)](interactive-program-set-cursor-in-field.html) | Sets the cursor in the specified field. |
| [void SetWindowShape(decimal, decimal)](interactive-program-set-window-shape.html) | Sets the window width and depth. |
| [void SetWindowLocation(decimal, decimal)](interactive-program-set-window-location.html) | Sets the window row and column position. |
| [void RetrieveWindowLocation()](interactive-program-retrieve-window-location.html) | Retrieves and adjusts the window location. |
| [void MoveWindowFields()](interactive-program-move-window-fields.html) | Moves window fields to the display. |
| [void clearCommandKeyIndicators()](interactive-program-clear-command-key-indicators.html) | Clears all command key indicators. |
| [void PromptForConfirmation()](interactive-program-prompt-for-confirmation.html) | Displays a confirmation prompt to the user. |
| [bool CheckUserPromptingAllowed()](interactive-program-check-user-prompting-allowed.html) | Checks whether user prompting is allowed. |
| [void CheckIsNumeric(string, string)](interactive-program-check-is-numeric.html) | Validates that a field contains a numeric value. |
| [void ValidateRequiredField(string, string)](interactive-program-validate-required-field.html) | Validates that a required field is not empty. |

## See Also
- [EscapeProgram](escape-program.html)
- [SingleRecordProgram](single-record-program.html)
- [SubfileProgram](subfile-program.html)
