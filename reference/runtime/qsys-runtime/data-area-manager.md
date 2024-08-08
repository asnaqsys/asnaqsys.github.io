---
title: "DataAreaManager class         | QSYS API Reference Guide"
description: "Handles DataArea operations. "
last_modified_at: 2024-08-08T21:41:46Z
---

Handles DataArea operations.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DataAreaManager()](#dataareamanager) | Creates a DataAreaManager object.

### DataAreaManager()

Creates a DataAreaManager object.

```cs
DataAreaManager()
```

## Methods

| Signature | Description |
| --- | --- |
| [In](#void-instring-name-database-db-string-path-bool-islock-bool-isvar-datastructure-ds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [DataStructure](/reference/runtime/qsys-runtime/data-structure.html)) | Reads from a DataArea into a DataStructure.
| [In](#object-instring-name-database-db-string-path-bool-islock-bool-isvar)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Reads from a DataArea.
| [Out](#void-outstring-name-bool-islock-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Writes a character value into a DataArea.
| [Out](#void-outstring-name-bool-islock-decimal-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Writes a decimal number into a DataArea.
| [Out](#void-outstring-name-bool-islock-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Writes a character string into a DataArea.
| [Out](#void-outstring-name-bool-islock-datastructure-ds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [DataStructure](/reference/runtime/qsys-runtime/data-structure.html)) | Writes a DataStructure object into a DataArea.
| [Out](#void-outstring-name-database-db-char-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Writes a character into a DataArea.
| [Out](#void-outstring-name-database-db-decimal-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Writes a decimal number into a DataArea.
| [Out](#void-outstring-name-database-db-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Writes a character string into a DataArea.
| [Out](#void-outstring-name-database-db-datastructure-ds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [DataStructure](/reference/runtime/qsys-runtime/data-structure.html)) | Writes an DataStructure object into a DataArea.
| [Unlock](#void-unlockstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Unlock a previously locked DataArea.
| [Unlock()](#void-unlock) | Unlock all the locked DataAreas in use.

### void In([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database db](/reference/runtime/qsys-runtime/database.html), [string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool isVar](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [DataStructure ds](/reference/runtime/qsys-runtime/data-structure.html))

Reads from a DataArea into a DataStructure.

```cs
void In(string name, Database db, string path, bool isLock, bool isVar, DataStructure ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Database](/reference/runtime/qsys-runtime/database.html) | db | Database instance.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | DataArea Database location.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isLock | True is locking should be performed; otherwise False.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isVar | False if the name parameter is a literal.
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ds | In ds param.

### object In([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database db](/reference/runtime/qsys-runtime/database.html), [string path](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool isVar](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Reads from a DataArea.

```cs
object In(string name, Database db, string path, bool isLock, bool isVar)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Database](/reference/runtime/qsys-runtime/database.html) | db | Database instance.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | DataArea Database location.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isLock | True is locking should be performed; otherwise False.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isVar | False if the name parameter is a literal.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The value retrieved from the data area.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Writes a character value into a DataArea.

```cs
void Out(string name, bool isLock, char value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isLock | If false it unlocks the DataArea; otherwise ignored.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | The character value to write into the DataArea.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [decimal value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Writes a decimal number into a DataArea.

```cs
void Out(string name, bool isLock, decimal value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isLock | If false it unlocks the DataArea; otherwise ignored.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The number to write into the DataArea.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Writes a character string into a DataArea.

```cs
void Out(string name, bool isLock, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isLock | If false it unlocks the DataArea; otherwise ignored.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The character string to write into the DataArea.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [DataStructure ds](/reference/runtime/qsys-runtime/data-structure.html))

Writes a DataStructure object into a DataArea.

```cs
void Out(string name, bool isLock, DataStructure ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isLock | If false it unlocks the DataArea; otherwise ignored.
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ds | The DataStructure object to write into the DataArea.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database db](/reference/runtime/qsys-runtime/database.html), [char value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Writes a character into a DataArea.

```cs
void Out(string name, Database db, char value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Database](/reference/runtime/qsys-runtime/database.html) | db | Database instance.
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | value | The new char value.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database db](/reference/runtime/qsys-runtime/database.html), [decimal value](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Writes a decimal number into a DataArea.

```cs
void Out(string name, Database db, decimal value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Database](/reference/runtime/qsys-runtime/database.html) | db | Database instance.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | value | The new decimal value.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database db](/reference/runtime/qsys-runtime/database.html), [string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Writes a character string into a DataArea.

```cs
void Out(string name, Database db, string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Database](/reference/runtime/qsys-runtime/database.html) | db | Database instance.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The new string value.

### void Out([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database db](/reference/runtime/qsys-runtime/database.html), [DataStructure ds](/reference/runtime/qsys-runtime/data-structure.html))

Writes an DataStructure object into a DataArea.

```cs
void Out(string name, Database db, DataStructure ds)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.
| [Database](/reference/runtime/qsys-runtime/database.html) | db | Database instance.
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | ds | The DataStructure object to write into the DataArea.

### void Unlock([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Unlock a previously locked DataArea.

```cs
void Unlock(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | DataArea name.

### void Unlock()

Unlock all the locked DataAreas in use.

```cs
void Unlock()
```
