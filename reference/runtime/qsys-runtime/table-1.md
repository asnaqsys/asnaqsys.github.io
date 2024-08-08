---
title: "Table&lt;T&gt; class          | QSYS API Reference Guide"
description: "Supports RPG&#39;s table type by encapsulating an array and providing it with an implied index through the use of the CurrentElement property. "
last_modified_at: 2024-08-08T21:41:46Z
---

Supports RPG's table type by encapsulating an array and providing it with an implied index through the use of the CurrentElement property.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Table](#tableint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Constructor for Table.

### Table([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Constructor for Table.

```cs
Table(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Number of elements within the array.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | CurrentElement | Returns the element at the current index of the Table. |
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Item | Default property for the table which returns the array value at the specified index. |

## Methods

| Signature | Description |
| --- | --- |
| [GetEnumerator()](#ienumerator-t-getenumerator) | Returns an enumerator to iterate over the table elements.

### IEnumerator<T> GetEnumerator()

Returns an enumerator to iterate over the table elements.

```cs
IEnumerator<T> GetEnumerator()
```
