---
title: "QueryValue class              | QSYS API Reference Guide"
description: "Represents a Value stored in a SQL Query Result. "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a Value stored in a SQL Query Result.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [QueryValue](#queryvalueobject)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Initializes a new instance of QueryValue class.

### QueryValue([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Initializes a new instance of QueryValue class.

```cs
QueryValue(Object)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | Initial value.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | Gets the underlying value  |

## Methods

| Signature | Description |
| --- | --- |
| [ToDateTime()](#datetime-todatetime) | Gets the underlying value by converting it to a DateTime object.
| [ToDecimal()](#decimal-todecimal) | Gets the underlying value by converting it to a Decimal object.
| [ToInt64()](#long-toint64) | Gets the underlying value by converting it to a Int64 object.
| [ToString()](#string-tostring) | Gets the underlying value by converting it to a String object.
| [ToTime()](#datetime-totime) | Gets the underlying value by converting it to a DateTime object.

### DateTime ToDateTime()

Gets the underlying value by converting it to a DateTime object.

```cs
DateTime ToDateTime()
```

### decimal ToDecimal()

Gets the underlying value by converting it to a Decimal object.

```cs
decimal ToDecimal()
```

### long ToInt64()

Gets the underlying value by converting it to a Int64 object.

```cs
long ToInt64()
```

### string ToString()

Gets the underlying value by converting it to a String object.

```cs
string ToString()
```

### DateTime ToTime()

Gets the underlying value by converting it to a DateTime object.

```cs
DateTime ToTime()
```
