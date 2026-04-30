---
title: "EscapeProgram Class"
description: "Abstract base class providing foundational infrastructure for all EscapeFX programs."
---


## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll  
**Inherits:** ASNA.QSys.Runtime.JobSupport.Program

Abstract base class providing foundational infrastructure for program execution, including initialization, messaging, data validation, database operations, and job management.

## Constructors

| Signature | Description |
| --- | --- |
| `EscapeProgram()` | Initializes a new instance, populating the program status data structure with job details. |

## Fields

| Type | Name | Description | Previous Name (PKA in Synon) |
| --- | --- | --- | --- |
| FixedDecimal<_6, _0> | AbsoluteDay1 | First absolute day value. | XDAY1 |
| FixedDecimal<_6, _0> | AbsoluteDay2 | Second absolute day value. | XDAY2 |
| FixedDecimal<_9, _0> | APIReturnCode | API return code. | W0RTW |
| FixedDecimal<_8, _0> | DateDuration | Calculated date duration. | XDURR |
| FixedString<_10> | DateListName | Date-list selection name. | WUDLN |
| FixedString<_3> | ExecutionEnvironment | The execution environment code. | W0ENV |
| FixedString<_1> | ExitLoop | Loop-exit flag state. | W0EXL |
| FixedString<_10> | FailedCalledProgram | The name of a failed called program. | W0CLPG |
| FixedString<_10> | FileInError | The file name currently in error. | ##EFL |
| FixedString<_1> | InitialCall | Initial-call state. | W0ICL |
| FixedString<_1> | IsWorkDay | The selected work-day indicator value. | XDSEL |
| DataStructure | JobDateTime_DS | Data structure for combined job date and time values. | JBDTTM |
| FixedDecimal<_7, _0> | JobExecStartDate | Job execution start date. | ##ED7 |
| FixedDecimal<_6, _0> | JobExecStartTime | Job execution start time. | ##ETM |
| FixedString<_10> | JobName | The current job name. | ##JOB |
| FixedDecimal<_6, _0> | JobNumber | Current job number. | ##JNO |
| FixedDecimal<_7, _0> | JobStartDate | Current job start date. | ##SD7 |
| FixedString<_10> | JobUserName | The current job user name. | ##USR, ZAUSR |
| FixedString<_25> | ListExternalValue | The external value for condition lists. | Y2EXVL |
| FixedString<_25> | ListInternalValue | The internal value for condition lists. | Y2INVL |
| FixedDecimal<_7, _0> | ListNumber | Current list number. | Y2LSNO |
| FixedString<_10> | MainFileLib | The main file library name. | ##FLB |
| FixedString<_10> | MainFileMbr | The main file member name. | ##FMB |
| FixedString<_10> | MainFileName | The main file name. | ##FFL |
| FixedString<_21> | MainFileQual | The qualified main file name. | ##FQL |
| DataStructure | MD0009_DS | Message-data structure used for message Y2U0009 payload composition. |  |
| FixedString<_7> | P0_ResultingCode | The public resulting code value. | P0RTN |
| FixedString<_10> | ProgramLibraryName | The current program library name. | ##PLB |
| FixedString<_10> | ProgramName | The current program name. | ##PGM |
| short | ProgramParmCount | The program parameter count. | ##PRM |
| FixedString<_1> | RecordDataChanged | Record-change state. | W0RDC |
| FixedString<_1> | RecordSelected | Record-selection state. | W0RSL |
| FixedString<_1> | ReloadSubfile | Subfile reload state. | W0RSF |
| FixedString<_1> | ReprocessCurrentRecord | Current-record reprocess state. | W0BNR |
| FixedString<_7> | ResultingCode | The internal resulting code value. | W0RTN |
| FixedString<_10> | SbmJobName | Submitted job name. | W0JVN |
| FixedString<_6> | SbmJobNumber | Submitted job number. | W0JNB |
| FixedString<_10> | SbmJobOverrideString | Submit-job override keywords. | W0SJO |
| FixedString<_10> | SbmJobUser | Submitted job user. | W0JUN |
| FixedString<_10> | SendMsgDefaultFile | Default message file name. | ZADFMF |
| FixedString<_10> | SendMsgFile | Message file name for send operations. | ZAMSGF |
| FixedString<_1> | SendMsgFirst | First-message flag state. | ZAFSMS |
| FixedString<_7> | SendMsgID | Message identifier. | ZAMSID |
| FixedString<_10> | SendMsgQueue | Target message queue name. | ZAPGMQ |
| FixedString<_5> | SendMsgQueuePos | Target queue position. | ZAPGRL |
| FixedString<_7> | SendMsgType | Message type code. | ZAMSTP |
| FixedString<_3> | SystemDateFormat | System date format code. | XDDTFM |
| FixedString<_1> | UserDefinedPrompting | User-defined prompting flag state. | W0PMT |
| FixedString<_25> | W0ConditionName | Resolved condition name. | W0CNNM |
| FixedString<_25> | W0InputValue | Working input value. | W0INVL |
| FixedString<_1> | W0ValueIsMapped | Mapped-value flag state. | W0VLMP |
| FixedDecimal<_15, _0> | W0Wrk150 | Decimal working field 150. | W0WJ |
| FixedDecimal<_15, _2> | W0Wrk152 | Decimal working field 152. | W0WA |
| FixedDecimal<_15, _5> | W0Wrk155 | Decimal working field 155. | W0WB |
| FixedDecimal<_17, _5> | W0Wrk175 | Decimal working field 175. | W0WC |
| FixedDecimal<_17, _7> | W0Wrk177 | Decimal working field 177. | W0WD |
| FixedDecimal<_17, _9> | W0Wrk179 | Decimal working field 179. | W0WE |
| FixedDecimal<_1, _0> | WorkDaysInWeek | Number of selected work days. | XDWSL |
| FixedStringArray<_7, _1> | WorkWeekDays | Selected work-week day markers. | YDOW |
| DataStructure | XDEX_DS | Data structure for external date representation. | XDEX |
| DataStructure | XDI2T_DS | Data structure for 10-character internal date representation. | XDI2T |
| DataStructure | XDI8T_DS | Data structure for 8-digit internal date representation. | XDI8T |
| DataStructure | XDINT_DS | Data structure for 7-digit internal date representation. | XDINT |
| FixedDecimal<_8, _0> | XDWK1 | Date-calculation work value. | XDWK1 |
| DataStructure | XTClock | Data structure for clock values. | XTCK |
| FixedDecimal<_5, _0> | ZQ | Generic decimal working field ZQ. | ZQ |

## Properties

| Signature | Description |
| --- | --- |
| `bool ResultingCodeIsOk { get; }` | Gets a value indicating whether the resulting code is blank (OK). |
| `bool ResultingCodeIsError { get; }` | Gets a value indicating whether the resulting code is non-blank (error). |
| `string SystemTimestamp { get; }` | Gets the current system timestamp in `yyyy-MM-dd-HH.mm.ss.ffffff` format. |

## Indicator Properties

The following boolean properties provide easy access to the global Indicator Array : _IN.  

In addition to generic `inXX` properties, this class significantly names the 3 indicators used for specific types of errors. 

| Type | Name | Description |
| --- | --- | --- |
| bool | in01 | Gets or sets the _IN[01] value. |
| bool | in02 | Gets or sets the _IN[02] value. |
| bool | in03 | Gets or sets the _IN[03] value. |
| ... | ... | ... |
| bool | in90 | Gets or sets the _IN[90] value. |
| bool | in90Error | Gets or sets the _IN[90] value. |
| bool | in91 | Gets or sets the _IN[91] value. |
| bool | in91IOError | Gets or sets the _IN[91] value. |
| bool | in92 | Gets or sets the _IN[92] value. |
| ... | ... | ... |
| bool | in98 | Gets or sets the _IN[98] value. |
| bool | in99 | Gets or sets the _IN[99] value. |
| bool | in99GlobalError | Gets or sets the _IN[99] value. |


## Methods

| Signature | Description |
| --- | --- |
| [void SetResultingCode(string)](escape-program-set-resulting-code.html) | Sets the resulting code to the specified message ID code. |
| [void ClearResultingCode()](escape-program-clear-resulting-code.html) | Clears the resulting code. |
| [void CheckForCallError(string, int[])](escape-program-check-for-call-error.html) | Checks for a program call error and sets the resulting code if one occurred. |
| [void VerifyCall(string, int[])](escape-program-verify-call.html) | Verifies a successful program call and issues a message if it ended in error. |
| [string SubstringWithPad(string, int, string)](escape-program-substring-with-pad.html) | Retrieves a substring from the start position to the end of the source. |
| [string SubstringWithPad(string, int, int, string)](escape-program-substring-with-pad.html) | Retrieves a fixed-length substring from the specified start position. |
| [string SubstringWithPad(string, decimal, decimal, string)](escape-program-substring-with-pad.html) | Retrieves a fixed-length substring using decimal start and length. |
| [bool FieldContainsPattern(string, string)](escape-program-field-contains-pattern.html) | Returns true if the field contains the specified pattern. |
| [decimal ScanField(string, string, char)](escape-program-scan-field.html) | Scans a string for a pattern, returning the 1-based position. |
| [decimal ScanField(string, int, int, string, int, bool, bool, char)](escape-program-scan-field.html) | Scans a string for a pattern with full control over target and pattern parameters. |
| [string TranslateWithTable(string, string, decimal, string)](escape-program-translate-with-table.html) | Translates a value using the specified translation table. |
| [string IsNotNumeric(string)](escape-program-is-not-numeric.html) | Returns "Y" if the string is not numeric, otherwise "N". |
| [decimal GetDateMonth(decimal)](escape-program-get-date-month.html) | Gets the month component from an internal date (CYYMMDD format). |
| [decimal GetDateYear(decimal)](escape-program-get-date-year.html) | Gets the year component from an internal date (CYYMMDD format). |
| [decimal DurationInDays(decimal, decimal, string, string)](escape-program-duration-in-days.html) | Calculates the number of work days between two internal dates. |
| [decimal DayOfWeek(decimal, string, string)](escape-program-day-of-week.html) | Determines the day of the week for an internal date. |
| [decimal ConvertToAbsoluteDay(decimal)](escape-program-convert-to-absolute-day.html) | Converts an internal date to an absolute day number from 01/01/01. |
| [void ConvertDateToDay()](escape-program-convert-date-to-day.html) | Converts the current InternalDate to AbsoluteDay1. |
| [void CalculateDurationDays()](escape-program-calculate-duration-days.html) | Calculates the duration in days between AbsoluteDay1 and AbsoluteDay2. |
| [decimal FormatDate(string)](escape-program-format-date.html) | Converts an internal date string (YYYY-MM-DD) to an external date with 2-digit year. |
| [decimal FormatDateYY(decimal)](escape-program-format-date-yy.html) | Converts an internal CYYMMDD date to an external 2-digit year format. |
| [decimal FormatDateYY8(decimal)](escape-program-format-date-yy8.html) | Converts an internal 8-digit YYYYMMDD date to an external 2-digit year format. |
| [decimal FormatDateYYYY8(decimal)](escape-program-format-date-yyyy8.html) | Converts an internal 8-digit YYYYMMDD date to an external 4-digit year format. |
| [decimal FormatDateYYYY(decimal)](escape-program-format-date-yyyy.html) | Converts an internal CYYMMDD date to an external 4-digit year format. |
| [decimal SynchronizeInternalDates(string)](escape-program-synchronize-internal-dates.html) | Sets the internal date fields from a yyyy-mm-dd string. |
| [string SynchronizeInternalDates(decimal)](escape-program-synchronize-internal-dates.html) | Sets the internal date fields from a decimal CYYMMDD value. |
| [void SetupDaysOfWeekArray(string, string)](escape-program-setup-days-of-week-array.html) | Initializes the days-of-week array for work-day calculations. |
| [void SendMessage()](escape-program-send-message.html) | Sends a message to the program's message queue. |
| [void SendMessage(string, string)](escape-program-send-message.html) | Sends a message with the specified ID and file. |
| [void SendErrorMessage(string, string, int[])](escape-program-send-error-message.html) | Sends an error message and sets error indicators. |
| [void SendErrorMessage(string, int[])](escape-program-send-error-message.html) | Sends an error message and sets error indicators using default message file. |
| [void SendCompletionMessage(string)](escape-program-send-completion-message.html) | Sends a completion message to the previous program queue. |
| [void SendInfoMessage(string)](escape-program-send-info-message.html) | Sends an informational message. |
| [void SendStatusMessage(string)](escape-program-send-status-message.html) | Sends a status message to the external queue. |
| [void ClearProgramMessages()](escape-program-clear-program-messages.html) | Clears all messages from the program's message queue. |
| [string RetrieveMessageText(string, string, string)](escape-program-retrieve-message-text.html) | Retrieves the first-level text of a message. |
| [virtual void CancelProgram()](escape-program-cancel-program.html) | Clears the resulting code and exits the program. |
| [virtual void ExitProgram()](escape-program-exit-program.html) | Copies messages to caller and terminates the program. |
| [FixedDecimal&lt;_6,_0&gt; GetTime6()](escape-program-get-time6.html) | Returns the current time as a 6-digit HHMMSS decimal. |
| [virtual void InitProgram()](escape-program-init-program.html) | Initializes program state, job date/time, and system defaults. |
| [virtual void InitMainFileInfo(DatabaseFileBase)](escape-program-init-main-file-info.html) | Populates main file context fields from the specified database file. |
| [string Y2QLVNR(string, string)](escape-program-y2qlvnr.html) | Returns an iSeries-style qualified object name. |
| [void CopyMessagesToCaller(string)](escape-program-copy-messages-to-caller.html) | Copies undisplayed messages to the caller's message queue. |
| [string YWRTLCI(string, decimal, decimal, string, ref decimal, ref decimal)](escape-program-ywrtlci.html) | Retrieves and adjusts a window location. |
| [string GetListExternalValue(string, int, string, string)](escape-program-get-list-external-value.html) | Retrieves the external value for an internal list value. |
| [string GetListInternalValue(string, int, string, string)](escape-program-get-list-internal-value.html) | Retrieves the internal value for an external list value. |
| [string RetrieveConditionName(string, int, string)](escape-program-retrieve-condition-name.html) | Retrieves the condition name for an internal value. |
| [string RetrieveMappedConditionName(string, int, string)](escape-program-retrieve-mapped-condition-name.html) | Retrieves the mapped condition name for an internal value. |
| [void ReadCurrentRecord(string, DatabaseFileBase)](escape-program-read-current-record.html) | Reads the current record from the specified file. |
| [bool LockForDelete(DatabaseFileBase, string, object[])](escape-program-lock-for-delete.html) | Locks a record for deletion. |
| [bool LockForDelete(string, DatabaseFileBase, string, object[])](escape-program-lock-for-delete.html) | Locks a record for deletion using the specified format name. |
| [bool LockForUpdate(DatabaseFileBase, string, object[])](escape-program-lock-for-update.html) | Locks a record for update. |
| [bool LockForUpdate(string, DatabaseFileBase, string, object[])](escape-program-lock-for-update.html) | Locks a record for update using the specified format name. |
| [void SendNoRecord(DatabaseFileBase, string, string)](escape-program-send-no-record.html) | Sends a "record not found" message. |
| [bool HasRecordChanged(DatabaseFileBase, string, string)](escape-program-has-record-changed.html) | Checks whether a record has changed since it was last read. |
| [void SubmitterNewRequest(string, string)](escape-program-submitter-new-request.html) | Initializes a new job submission request. |
| [void SubmitterAddCharArgument(string, int)](escape-program-submitter-add-char-argument.html) | Adds a character argument to the job submission request. |
| [void SubmitterAddPackArgument(decimal, int, int)](escape-program-submitter-add-pack-argument.html) | Adds a packed decimal argument to the job submission request. |
| [void SubmitterSubmit()](escape-program-submitter-submit.html) | Submits the job request. |

## See Also
- [InteractiveProgram](interactive-program.html)
- [PrintFunction](print-function.html)
- [ExternalFunction](external-function.html)