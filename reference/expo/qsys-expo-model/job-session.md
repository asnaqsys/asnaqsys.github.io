---
title: "JobSession class              | QSYS API Reference Guide"
description: "Stores user data while the user navigates the application. JobSession state uses a store maintained by the Job to persist data across requests. "
last_modified_at: 2024-08-09T17:26:04Z
---

Stores user data while the user navigates the application. JobSession state uses a store maintained by the Job to persist data across requests.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
The `JobSession` state uses a store maintained by the Job to persist data across requests.

To get a reference to `JobSession` instance use the [`Command.JobSession`](/reference/expo/qsys-expo-model/job-session.html) property.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CommandParm | Gets or sets the Parameter used by Outsite Pages name from/to the Session |
| [Byte\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | EnabledKeys | Gets or sets an array of bytes representing the cached enabled keys |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | TransactionID | Gets or sets the Job Number from/to the Session |

## Methods

| Signature | Description |
| --- | --- |
| [ContainsUserKey](#bool-containsuserkeystring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the JobSession contains the specified user key.
| [GetUserInt32](#int-getuserint32string-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get a 32-bit integer value to a user provided key in the JobSession.
| [GetUserString](#string-getuserstringstring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get a string value to a user provided key in the JobSession.
| [RemoveUserValue](#void-removeuservaluestring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes the value referenced by a user key
| [SetUserInt32](#void-setuserint32string-key-int-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Set a 32-bit integer value to a user provided key in the JobSession.
| [SetUserString](#void-setuserstringstring-key-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Set a string value to a user provided key in the JobSession.

### bool ContainsUserKey([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether the JobSession contains the specified user key.

```cs
bool ContainsUserKey(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | The key to locate.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the JobSession contains an element with the specified key; otherwise, false.

### int GetUserInt32([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get a 32-bit integer value to a user provided key in the JobSession.

```cs
int GetUserInt32(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | User Key to the number.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The stored value.

### string GetUserString([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get a string value to a user provided key in the JobSession.

```cs
string GetUserString(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | User Key to the string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The stored value.

### void RemoveUserValue([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes the value referenced by a user key

```cs
void RemoveUserValue(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | User Key to the value

### void SetUserInt32([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Set a 32-bit integer value to a user provided key in the JobSession.

```cs
void SetUserInt32(string key, int value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | User key to the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | value | The numeric value.

### void SetUserString([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Set a string value to a user provided key in the JobSession.

```cs
void SetUserString(string key, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | User key to the string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The string value.
