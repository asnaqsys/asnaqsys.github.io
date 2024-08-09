---
title: "MessageFileReader class       | QSYS API Reference Guide"
description: "Provides the contents of a message file. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides the contents of a message file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [MessageFileReader](#messagefilereaderstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of ASNA.QSys.Runtime.MessageFileReaderclass.

### MessageFileReader([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of ASNA.QSys.Runtime.MessageFileReaderclass.

```cs
MessageFileReader(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName |             The name of the compiled message file.            

## Methods

| Signature | Description |
| --- | --- |
| [GetMessageText](#string-getmessagetextstring-prefix-int-id)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the message text from the specified prefix and id number.
| [GetMessageText](#string-getmessagetextstring-prefix-int-id-object--replacementvalues)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the message text from the specified prefix and id number, and assigns the replacement text for the symbolic placeholders put in the message file.
| [GetSecondMessageText](#string-getsecondmessagetextstring-prefix-int-id)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the second level message text from the specified prefix and id number.
| [GetSecondMessageText](#string-getsecondmessagetextstring-prefix-int-id-object--replacementvalues)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the second level message text from the specified prefix and id number,and assigns the replacement text for the symbolic placeholders put in the second level text of the message file.
| [InsertReplacementValues](#string-insertreplacementvaluesstring-text-object--replacementvalues)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Creates a formatted string given an IBM-style message with replacement characters and corresponding replacement values.

### string GetMessageText([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int id](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the message text from the specified prefix and id number.

```cs
string GetMessageText(string prefix, int id)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix |             The 3 character string prefix under which the requested message is stored.            
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | id |             The numeric value under which the requested message is stored.            

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### string GetMessageText([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int id](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Object\[\] replacementValues](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Gets the message text from the specified prefix and id number, and assigns the replacement text for the symbolic placeholders put in the message file.

```cs
string GetMessageText(string prefix, int id, Object[] replacementValues)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix |             The 3 character string prefix under which the requested message is stored.            
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | id |             The numeric value under which the requested message is stored.            
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | replacementValues |             An array of objects meant to replace the symbolic placeholders placed            in the message file.            

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### string GetSecondMessageText([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int id](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the second level message text from the specified prefix and id number.

```cs
string GetSecondMessageText(string prefix, int id)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix |             The 3 character string prefix under which the requested message is stored.            
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | id |             The numeric value under which the requested message is stored.            

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### string GetSecondMessageText([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int id](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Object\[\] replacementValues](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Gets the second level message text from the specified prefix and id number,and assigns the replacement text for the symbolic placeholders put in the second level text of the message file.

```cs
string GetSecondMessageText(string prefix, int id, Object[] replacementValues)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix |             The 3 character string prefix under which the requested message is stored.            
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | id |             The numeric value under which the requested message is stored.            
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | replacementValues |             An array of objects meant to replace the symbolic placeholders placed            in the second level text of the message file.            

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### string InsertReplacementValues([string text](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] replacementValues](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Creates a formatted string given an IBM-style message with replacement characters and corresponding replacement values.

```cs
string InsertReplacementValues(string text, Object[] replacementValues)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The IBM-style message string.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | replacementValues | An array of replacements to insert in the message string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The formatted string.
