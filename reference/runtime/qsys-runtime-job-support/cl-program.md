---
title: "CLProgram class               | QSYS API Reference Guide"
description: "Defines the core behavior of programs migrated from CL program . "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the core behavior of programs migrated from CL program .

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Module](/reference/runtime/qsys-runtime-job-support/module.html) --> [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html) --> [Program](/reference/runtime/qsys-runtime-job-support/program.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [CLProgram()](#clprogram) | Initializes a new instance of the CLProgram class.

### CLProgram()

Initializes a new instance of the CLProgram class.

```cs
CLProgram()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [List\<Type\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | exceptionToIgnoreList | List of exceptions to ignore on certain commands. |

## Methods

| Signature | Description |
| --- | --- |
| [AddLibLEntry](#void-addliblentrystring-libraryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a library name to the start of the user portion of library list.
| [AddLibLEntry](#void-addliblentrystring-libraryname-liblposition-position-string-referencelibraryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [LiblPosition](/reference/datagate/datagate-client/libl-position.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a library name at a particular position in the user portion of the library list.
| [AddLogicalFileMember](#void-addlogicalfilememberstring-file-string-member-string--datamembers-string-text)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds a member to a logical file.
| [AddMsgToIgnore](#void-addmsgtoignoretype-exceptiontype)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Add an exception to the list of exceptions to ignore.
| [AddPFM](#void-addpfmstring-file-string-mbr-string-text-string-srctype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Add a member to a physical file.
| [Asterisk_BCat](#string-asterisk-bcatstring-prefix-string-suffix)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Concatenates two strings, trimming the end of the first string and adding a blank between the two strings.
| [Asterisk_TCat](#string-asterisk-tcatstring-prefix-string-suffix)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Concatenates two strings trimming all blanks from the first string.
| [ChangeDataArea](#void-changedataareastring-dataarea-string-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Update the contents of a character data area.
| [ChangeDataArea](#void-changedataareastring-dataarea-int-start-int-length-string-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Update a portion of a character data area.
| [ChangeDataArea](#void-changedataareastring-dataarea-decimal-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Update the contents of a decimal data area.
| [ChangeDataArea](#void-changedataareastring-dataarea-bool-newvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Update the contents of a logical data area.
| [ChangeFileMemberText](#void-changefilemembertextstring-file-string-mbr-string-newtext)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Change the Text attribute of a file member.
| [ClearPFM](#void-clearpfmstring-file-string-mbr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Remove all records from a file's member.
| [ConvertDate](#string-convertdatestring-date-string-fromdateformat-string-todatefmt-string-todatesep)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a string representing a date in one format to a string with the date formatted in another format.
| [CreateDataArea](#void-createdataareastring-library-string-dataareaname-int-len-string-initvalue-string-text)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a new character data area.
| [CreateDecDataArea](#void-createdecdataareastring-library-string-dataareaname-int-len-int-decimals-decimal-initvalue-string-text)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a new decimal data area.
| [CreateDuplicateFile](#void-createduplicatefilestring-fromlibrary-string-filename-string-tolibrary-string-newname-bool-copydata)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Create a copy of an existing file.
| [CreateLglDataArea](#void-createlgldataareastring-library-string-dataareaname-char-initvalue-string-text)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a logical data area capable of holding a value of '1' or '0'.
| [DataAreaExists](#bool-dataareaexistsstring-library-string-dataarea)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Check for existence of a data area.
| [DelayJob_ResumeTime](#void-delayjob-resumetimestring-hhmmss)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Suspends the execution on the job until a specific time in the future.
| [DelayJob_Seconds](#void-delayjob-secondsdecimal-seconds)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Suspends the execution on the job for the specified time.
| [DelayJob_Seconds](#void-delayjob-secondsulong-seconds)([UInt64](https://docs.microsoft.com/en-us/dotnet/api/system.uint.64)) | Suspends the execution on the job for the specified time.
| [DelayJob_Seconds](#void-delayjob-secondsint-seconds)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Suspends the execution on the job for the specified time.
| [DeleteDataArea](#void-deletedataareastring-dataarea)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete an existing data area.
| [DeleteFile](#void-deletefilestring-filepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete a file database or printer file.
| [DeleteOverride](#void-deleteoverridestring-filename-overridescope-scope)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [OverrideScope](/reference/runtime/qsys-runtime-job-support/override-scope.html)) | Removes a previous override for a file. 
| [FileExists](#bool-fileexistsstring-filepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Test for the existence of a database or printer file.
| [InitializePFM](#void-initializepfmstring-file-string-mbr-initializepfmoption-records-int-totrcds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [InitializePFMOption](/reference/runtime/qsys-runtime-job-support/initialize-pfm-option.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initialize records in a physical file member.
| [InitializePFM](#void-initializepfmstring-file-string-mbr-int-totrcds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initialize a physical file member with records containing their field's default values.
| [LibraryExists](#bool-libraryexistsstring-libraryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Test for the existence of a database library.
| [MemberExists](#bool-memberexistsstring-filepath-string-membername)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Test for the existence of a database file's member.
| [OverrideFile](#void-overridefilestring-filename-overrideoption-option-object-newvalue-overridescope-scope)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [OverrideOption](/reference/runtime/qsys-runtime-job-support/override-option.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [OverrideScope](/reference/runtime/qsys-runtime-job-support/override-scope.html)) | Temporary overrides (replaces) a file name, its location or some other parameter used when a program opens the file.
| [Percent_SST](#void-percent-sststring-receiver-int-start-int-length-string-value)([String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves a substring. The substring starts at a specified position and has a specified length.
| [Percent_Switch](#string-percent-switchstring-mask)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Tests the current state of the job's switches.
| [RemoveMember](#void-removememberstring-file-string-mbr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete a member from a database file.
| [RenameDataArea](#void-renamedataareastring-dataareaname-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Rename a data area.
| [RenameFile](#void-renamefilestring-filename-string-newfilename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Rename a database or printer file.
| [RenameFileMember](#void-renamefilememberstring-file-string-mbr-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Change the Name of a file member.
| [ResetAttentionProgram()](#void-resetattentionprogram) | Resets the attention program settings to the previous invocation level.
| [RetrieveDataArea](#string-retrievedataareastring-dataarea)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value of a data area.
| [RetrieveDataArea](#string-retrievedataareastring-dataarea-int-start-int-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a portion of a data area.
| [RetrieveJobAttribute](#string-retrievejobattributejobstringattribute-jobattribute)([JobStringAttribute](/reference/runtime/qsys-runtime-job-support/job-string-attribute.html)) | Gets an attribute of the current job.
| [RetrieveMemberDescription](#decimal-retrievememberdescriptionstring-file-string-mbr-memberdecimaldescription-descriptionattribute)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MemberDecimalDescription](/reference/runtime/qsys-runtime-job-support/member-decimal-description.html)) | Gets a numeric attribute of a file member.
| [RetrieveMemberDescription](#string-retrievememberdescriptionstring-file-string-mbr-memberstringdescription-descriptionattribute)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MemberStringDescription](/reference/runtime/qsys-runtime-job-support/member-string-description.html)) | Gets a string attribute of a file member.
| [RetrieveMessage](#string-retrievemessagestring-msgid-string-msgfile-string-msgdata)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Produces the strings with the formatted first and second level text for a message. Any placeholders are replaced with values from the message data. 
| [RmvLibLEntry](#void-rmvliblentrystring-libraryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a library name from the user portion of the library list.
| [SetAttentionProgram](#void-setattentionprogrambool-invokeprogram)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Enables or disables the current Attention Program.
| [SetAttentionProgram](#void-setattentionprogramstring-assemblyname-string-programname-bool-invokeprogram)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Sets the attention program to be be called when the Attention Key is 'pressed'
| [splitQualifiedNameForInput](#string-splitqualifiednameforinputstring-qualifiedname-string-library-string-objectname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Separate the name components of a qualified name.
| [splitQualifiedNameForOutput](#string-splitqualifiednameforoutputstring-qualifiedname-string-library-string-objectname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Separate the name components of a qualified name.
| [TryAddLibLEntry](#bool-tryaddliblentrystring-libraryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Attempts to add a library name to the start of the user portion of library list.
| [TryAddLibLEntry](#bool-tryaddliblentrystring-libraryname-liblposition-position-string-referencelibraryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [LiblPosition](/reference/datagate/datagate-client/libl-position.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Attempts to add a library name at a particular position in the user portion of the library list.

### void AddLibLEntry([string libraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a library name to the start of the user portion of library list.

```cs
void AddLibLEntry(string libraryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | libraryName | The name of the library.

### void AddLibLEntry([string libraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [LiblPosition position](/reference/datagate/datagate-client/libl-position.html), [string referenceLibraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a library name at a particular position in the user portion of the library list.

```cs
void AddLibLEntry(string libraryName, LiblPosition position, string referenceLibraryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | libraryName | The name of the library.
| [LiblPosition](/reference/datagate/datagate-client/libl-position.html) | position | One of the enumeration values that specifies the position where to add the name. May be absolute or relative.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | referenceLibraryName | For relative position values it specifies the refererence point.

### void AddLogicalFileMember([string file](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string member](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] dataMembers](https://docs.microsoft.com/en-us/dotnet/api/system.string), [string text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds a member to a logical file.

```cs
void AddLogicalFileMember(string file, string member, String[] dataMembers, string text)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | file | The name of logical file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | member | The name of the new file's member.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataMembers | An array of the physical file members with the data of the new logical member.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The text description of the new member.

### void AddMsgToIgnore([Type exceptionType](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Add an exception to the list of exceptions to ignore.

```cs
void AddMsgToIgnore(Type exceptionType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | exceptionType | Excption to ignore.

### void AddPFM([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string srcType](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Add a member to a physical file.

```cs
void AddPFM(string File, string Mbr, string Text, string srcType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | New member name to add.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Text | The text description of the new member.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | srcType | Content type for members of source files.

### string Asterisk_BCat([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string suffix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Concatenates two strings, trimming the end of the first string and adding a blank between the two strings.

```cs
string Asterisk_BCat(string prefix, string suffix)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix | The first part of the new string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | suffix | The last part of the new string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The concatenation of the two string.

### string Asterisk_TCat([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string suffix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Concatenates two strings trimming all blanks from the first string.

```cs
string Asterisk_TCat(string prefix, string suffix)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix | The first part of the new string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | suffix | The last part of the new string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The concatenation of the two string.

### void ChangeDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Update the contents of a character data area.

```cs
void ChangeDataArea(string dataArea, string newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | Path to the data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | New value of the character data area.

### void ChangeDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Update a portion of a character data area.

```cs
void ChangeDataArea(string dataArea, int start, int length, string newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | Path to the data area.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-base index to the first character to start updating.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the value to modify.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | New value of the character data area.

### void ChangeDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal newValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Update the contents of a decimal data area.

```cs
void ChangeDataArea(string dataArea, decimal newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | Path to the data area.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | newValue | New value of the decimal data area.

### void ChangeDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool newValue](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Update the contents of a logical data area.

```cs
void ChangeDataArea(string dataArea, bool newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | Path to the data area.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | newValue | New value of the logical data area.

### void ChangeFileMemberText([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string NewText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Change the Text attribute of a file member.

```cs
void ChangeFileMemberText(string File, string Mbr, string NewText)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | Name of member.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewText | New Text.

### void ClearPFM([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Remove all records from a file's member.

```cs
void ClearPFM(string File, string Mbr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | Name of member to be cleared.

### string ConvertDate([string date](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string fromDateFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string toDateFmt](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string toDateSep](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts a string representing a date in one format to a string with the date formatted in another format.

```cs
string ConvertDate(string date, string fromDateFormat, string toDateFmt, string toDateSep)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | date | The input string date to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fromDateFormat | The format in the input string. Defaults to "*JOB".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDateFmt | The desired format on the output string. Defaults to "*JOB".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDateSep | The character to use as the separator in output string. Defaults to "*JOB".

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The date in the desired format.

### void CreateDataArea([string library](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string dataAreaName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string initValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Create a new character data area.

```cs
void CreateDataArea(string library, string dataAreaName, int len, string initValue, string text)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The name of the library that will contain the new data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataAreaName | The name of the new data area.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | The length of the data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | initValue | The initial value of the data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The text describing the data area.

### void CreateDecDataArea([string library](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string dataAreaName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int len](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal initValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [string text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Create a new decimal data area.

```cs
void CreateDecDataArea(string library, string dataAreaName, int len, int decimals, decimal initValue, string text)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The name of the library that will contain the new data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataAreaName | The name of the new data area.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | len | The number of digits that the data area values can have.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal digit for the data area value.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | initValue | The initial value of the data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The text describing the data area.

### void CreateDuplicateFile([string FromLibrary](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string FileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string ToLibrary](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string NewName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool CopyData](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Create a copy of an existing file.

```cs
void CreateDuplicateFile(string FromLibrary, string FileName, string ToLibrary, string NewName, bool CopyData)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FromLibrary | The library name of the existing file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | The name of the existing file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ToLibrary | The library name where the new file will be.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewName | The name of the new file.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CopyData | true to copy the records of the existing file to the new file; otherwise, false.

### void CreateLglDataArea([string library](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string dataAreaName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [char initValue](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char), [string text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Create a logical data area capable of holding a value of '1' or '0'.

```cs
void CreateLglDataArea(string library, string dataAreaName, char initValue, string text)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The name of the library that will contain the new data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataAreaName | The name of the new data area.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | initValue | The initial value of the data area.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The text describing the data area.

### bool DataAreaExists([string library](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Check for existence of a data area.

```cs
bool DataAreaExists(string library, string dataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The library where the data area may be located.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | The name of the data area.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the data area exists; otherwise false.

### void DelayJob_ResumeTime([string hhmmss](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Suspends the execution on the job until a specific time in the future.

```cs
void DelayJob_ResumeTime(string hhmmss)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | hhmmss | The future time of day to resume execution. The clock format is two digits for each of: hour, minute, second.

### void DelayJob_Seconds([decimal seconds](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Suspends the execution on the job for the specified time.

```cs
void DelayJob_Seconds(decimal seconds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | seconds | The amount of seconds to sleep.

### void DelayJob_Seconds([ulong seconds](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Suspends the execution on the job for the specified time.

```cs
void DelayJob_Seconds(ulong seconds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [UInt64](https://docs.microsoft.com/en-us/dotnet/api/system.uint.64) | seconds | The amount of seconds to sleep.

### void DelayJob_Seconds([int seconds](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Suspends the execution on the job for the specified time.

```cs
void DelayJob_Seconds(int seconds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | seconds | The amount of seconds to sleep.

### void DeleteDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete an existing data area.

```cs
void DeleteDataArea(string dataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | The qualified path to the data area.

### void DeleteFile([string FilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete a file database or printer file.

```cs
void DeleteFile(string FilePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FilePath | Qualified file name (library/file).

### void DeleteOverride([string fileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [OverrideScope scope](/reference/runtime/qsys-runtime-job-support/override-scope.html))

Removes a previous override for a file. 

```cs
void DeleteOverride(string fileName, OverrideScope scope)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | The simple file name used by programs.
| [OverrideScope](/reference/runtime/qsys-runtime-job-support/override-scope.html) | scope | One of the enumeration values that specifies the scope of the override. If not given CallLvl is used.

### bool FileExists([string FilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Test for the existence of a database or printer file.

```cs
bool FileExists(string FilePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FilePath | Qualified file name (library/file).

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the file exists; otherwise, false.

### void InitializePFM([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [InitializePFMOption Records](/reference/runtime/qsys-runtime-job-support/initialize-pfm-option.html), [int TotRcds](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Initialize records in a physical file member.

```cs
void InitializePFM(string File, string Mbr, InitializePFMOption Records, int TotRcds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | Name of member to be initialized.
| [InitializePFMOption](/reference/runtime/qsys-runtime-job-support/initialize-pfm-option.html) | Records | One of enumeration values that specifies the type of data to include in the new records.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | TotRcds | The number of records the member should contain when the operation ends.

### void InitializePFM([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int TotRcds](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Initialize a physical file member with records containing their field's default values.

```cs
void InitializePFM(string File, string Mbr, int TotRcds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | Name of member to be initialized.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | TotRcds | The number of records the member should contain when the operation ends.

### bool LibraryExists([string LibraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Test for the existence of a database library.

```cs
bool LibraryExists(string LibraryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | LibraryName | The name of the library being tested.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the library exists; otherwise, false.

### bool MemberExists([string FilePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MemberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Test for the existence of a database file's member.

```cs
bool MemberExists(string FilePath, string MemberName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FilePath | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MemberName | Member name or *FIRST

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the member exists, false otherwise

### void OverrideFile([string fileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [OverrideOption option](/reference/runtime/qsys-runtime-job-support/override-option.html), [object newValue](https://docs.microsoft.com/en-us/dotnet/api/system.object), [OverrideScope scope](/reference/runtime/qsys-runtime-job-support/override-scope.html))

Temporary overrides (replaces) a file name, its location or some other parameter used when a program opens the file.

```cs
void OverrideFile(string fileName, OverrideOption option, object newValue, OverrideScope scope)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | The simple file name used by programs.
| [OverrideOption](/reference/runtime/qsys-runtime-job-support/override-option.html) | option | One of the enumeration values that specifies the parameter to override.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | newValue | The value to use when the file is used.
| [OverrideScope](/reference/runtime/qsys-runtime-job-support/override-scope.html) | scope | One of the enumeration values that specifies the scope of the override. If not given CallLvl is used.

### void Percent_SST([String& receiver](https://docs.microsoft.com/en-us/dotnet/api/system.string), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Retrieves a substring. The substring starts at a specified position and has a specified length.

```cs
void Percent_SST(String& receiver, int start, int length, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | receiver | The receiver of the substring.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based position of the substring start.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the substring.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The string containing the substring.

### string Percent_Switch([string mask](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Tests the current state of the job's switches.

```cs
string Percent_Switch(string mask)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | A positional list of up to 8 '1'/'0' values corresponding to the job's switches to be tested.  Use any other character, like an 'X', for switches to be ignored.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | "1" if the switches match the mask; otherwise, "0".

### void RemoveMember([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete a member from a database file.

```cs
void RemoveMember(string File, string Mbr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | Name of member to remove.

### void RenameDataArea([string dataAreaName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Rename a data area.

```cs
void RenameDataArea(string dataAreaName, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataAreaName | Qualified data area name (library/dataarea).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New simple data area name.

### void RenameFile([string fileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Rename a database or printer file.

```cs
void RenameFile(string fileName, string newFileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newFileName | New simple file name.

### void RenameFileMember([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string NewName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Change the Name of a file member.

```cs
void RenameFileMember(string File, string Mbr, string NewName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | Qualified file name (library/file).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | Name of member.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NewName | Member new name.

### void ResetAttentionProgram()

Resets the attention program settings to the previous invocation level.

```cs
void ResetAttentionProgram()
```

### string RetrieveDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the value of a data area.

```cs
string RetrieveDataArea(string dataArea)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | Path to the data area.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value stored on the data area.

### string RetrieveDataArea([string dataArea](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a portion of a data area.

```cs
string RetrieveDataArea(string dataArea, int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataArea | Path to the data area.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-base index to the first character to start updating.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length of the value to modify.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value stored on the data area portion.

### string RetrieveJobAttribute([JobStringAttribute jobAttribute](/reference/runtime/qsys-runtime-job-support/job-string-attribute.html))

Gets an attribute of the current job.

```cs
string RetrieveJobAttribute(JobStringAttribute jobAttribute)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [JobStringAttribute](/reference/runtime/qsys-runtime-job-support/job-string-attribute.html) | jobAttribute | One of the enumeration values that specifes what attribute to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The requested attributed.

### decimal RetrieveMemberDescription([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MemberDecimalDescription DescriptionAttribute](/reference/runtime/qsys-runtime-job-support/member-decimal-description.html))

Gets a numeric attribute of a file member.

```cs
decimal RetrieveMemberDescription(string File, string Mbr, MemberDecimalDescription DescriptionAttribute)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | The qualified name of the file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | The name of the member.
| [MemberDecimalDescription](/reference/runtime/qsys-runtime-job-support/member-decimal-description.html) | DescriptionAttribute | The requested description attribute.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The value of the attribute requested.

### string RetrieveMemberDescription([string File](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Mbr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MemberStringDescription DescriptionAttribute](/reference/runtime/qsys-runtime-job-support/member-string-description.html))

Gets a string attribute of a file member.

```cs
string RetrieveMemberDescription(string File, string Mbr, MemberStringDescription DescriptionAttribute)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | File | The qualified name of the file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Mbr | The name of the member.
| [MemberStringDescription](/reference/runtime/qsys-runtime-job-support/member-string-description.html) | DescriptionAttribute | The requested description attribute.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of the attribute requested.

### string RetrieveMessage([string MsgId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgFile](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgData](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Produces the strings with the formatted first and second level text for a message. Any placeholders are replaced with values from the message data. 

```cs
string RetrieveMessage(string MsgId, string MsgFile, string MsgData)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgFile | The message file name where the message description is to be found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgId | The message identification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgData | The replacement text, if any, for the message placeholders.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The formatted first level text of the message.

### void RmvLibLEntry([string libraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes a library name from the user portion of the library list.

```cs
void RmvLibLEntry(string libraryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | libraryName | The name of the library to remove from the list.

### void SetAttentionProgram([bool invokeProgram](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Enables or disables the current Attention Program.

```cs
void SetAttentionProgram(bool invokeProgram)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | invokeProgram | true to enable; otherwise, false.

### void SetAttentionProgram([string assemblyName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string programName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool invokeProgram](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Sets the attention program to be be called when the Attention Key is 'pressed'

```cs
void SetAttentionProgram(string assemblyName, string programName, bool invokeProgram)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | assemblyName | Name of assembly that contains the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | Qualified name of the class implementing the program logic.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | invokeProgram | true to enable.

### string splitQualifiedNameForInput([string qualifiedName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String& library](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String& objectName](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Separate the name components of a qualified name.

```cs
string splitQualifiedNameForInput(string qualifiedName, String& library, String& objectName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qualifiedName | Qualified name to dissect.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The library name. If there is no library component, "*LIBL" is returned.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | objectName | The object name.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The fully qualified name.

### string splitQualifiedNameForOutput([string qualifiedName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String& library](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String& objectName](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Separate the name components of a qualified name.

```cs
string splitQualifiedNameForOutput(string qualifiedName, String& library, String& objectName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qualifiedName | Qualified name to dissect.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | library | The library name. If there is no library component, "*CURLIB" is returned.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | objectName | The object name.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The fully qualified name.

### bool TryAddLibLEntry([string libraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Attempts to add a library name to the start of the user portion of library list.

```cs
bool TryAddLibLEntry(string libraryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | libraryName | The name of the library.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the library was added successfully; otherwise, false. 

### bool TryAddLibLEntry([string libraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [LiblPosition position](/reference/datagate/datagate-client/libl-position.html), [string referenceLibraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Attempts to add a library name at a particular position in the user portion of the library list.

```cs
bool TryAddLibLEntry(string libraryName, LiblPosition position, string referenceLibraryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | libraryName | The name of the library to add.
| [LiblPosition](/reference/datagate/datagate-client/libl-position.html) | position | One of the enumeration values that specifies the position where to add the name. May be absolute or relative.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | referenceLibraryName | For name of the library to use as a reference point for relative position values.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the library was added successfully; otherwise, false. 
