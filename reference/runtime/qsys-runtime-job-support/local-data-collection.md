---
title: "LocalDataCollection class     | QSYS API Reference Guide"
description: "Represents a versioned collection of name/value pairs. "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a versioned collection of name/value pairs.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [LocalDataCollection()](#localdatacollection) | Initializes a new, empty instance of the LocalDataCollection class.

### LocalDataCollection()

Initializes a new, empty instance of the LocalDataCollection class.

```cs
LocalDataCollection()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Count | Gets the number of key/value pairs contained in the LocalDataCollection. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Item | Gets or sets the value associated with the specified name. Setting a value increments the LocalDataCollection version. |
| [ICollection](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | Names | Gets an ICollection containing the names in the LocalDataCollection. |
| [ICollection](https://docs.microsoft.com/en-us/dotnet/api/system.collections.icollection) | Values | Gets an ICollection containing the values in the LocalDataCollection. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Version | Gets the version of the LocalDataCollection. |

## Methods

| Signature | Description |
| --- | --- |
| [Add](#void-addstring-name-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds an element with the specified key and value into the LocalDataCollection. Adding an element increments the LocalDataCollection version.
| [Clear()](#void-clear) | Removes all elements from the LocalDataCollection. Clearing the LocalDataCollection increments its version.
| [Contains](#bool-containsstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the LocalDataCollection contains a specific name.
| [GetEnumerator()](#idictionaryenumerator-getenumerator) | Returns an IDictionaryEnumerator that iterates through the LocalDataCollection.
| [Remove](#void-removestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes the element with the specified key from the LocalDataCollection. Removing an element increments the version of the LocalDataCollection.
| [RemoveAll()](#void-removeall) | Removes all elements from the LocalDataCollection. Clearing the LocalDataCollection increments its version.

### void Add([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Adds an element with the specified key and value into the LocalDataCollection. Adding an element increments the LocalDataCollection version.

```cs
void Add(string name, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name whose value to get or set.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The value of the element to add.

### void Clear()

Removes all elements from the LocalDataCollection. Clearing the LocalDataCollection increments its version.

```cs
void Clear()
```

### bool Contains([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether the LocalDataCollection contains a specific name.

```cs
bool Contains(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The key to locate in the LocalDataCollection.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the LocalDataCollection contains 

### IDictionaryEnumerator GetEnumerator()

Returns an IDictionaryEnumerator that iterates through the LocalDataCollection.

```cs
IDictionaryEnumerator GetEnumerator()
```

### void Remove([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes the element with the specified key from the LocalDataCollection. Removing an element increments the version of the LocalDataCollection.

```cs
void Remove(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the element to remove.

### void RemoveAll()

Removes all elements from the LocalDataCollection. Clearing the LocalDataCollection increments its version.

```cs
void RemoveAll()
```
