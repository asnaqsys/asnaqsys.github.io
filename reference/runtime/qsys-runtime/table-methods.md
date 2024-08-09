---
title: "TableMethods class            | QSYS API Reference Guide"
description: "Contains extension methods for handling Table RPG semantics. "
last_modified_at: 2024-08-09T16:18:25Z
---

Contains extension methods for handling Table RPG semantics.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Lookup\<T\>](#bool-lookup-t-table-t-table-t-searchargument-searchtype-searchtype-indicator-ind)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType](/reference/runtime/qsys-runtime/search-type.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Searches the Table for the specified search argument.
| [Lookup\<T\>](#bool-lookup-t-table-t-table-t-searchargument-searchtype-searchtype-indicator-hiloind-indicator-eqind)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType](/reference/runtime/qsys-runtime/search-type.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Searches the Table for the specified search argument.
| [Lookup\<T\>](#bool-lookup-t-table-t-table-t-searchargument)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Searches the Table for the specified search argument.
| [Lookup\<T, U\>](#bool-lookup-t-u-table-t-table-t-searchargument-searchtype-searchtype-table-u-result-indicator-ind)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType](/reference/runtime/qsys-runtime/search-type.html), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Searches the Table for the specified search argument.
| [Lookup\<T, U\>](#bool-lookup-t-u-table-t-table-t-searchargument-searchtype-searchtype-table-u-result-indicator-hiloind-indicator-eqind)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType](/reference/runtime/qsys-runtime/search-type.html), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html), [Indicator&](/reference/runtime/qsys-runtime/indicator.html)) | Searches the Table for the specified search argument.
| [Lookup\<T, U\>](#bool-lookup-t-u-table-t-table-t-searchargument-table-u-alttable)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html)) | Searches the Table for the specified search argument.
| [LookupGE\<T\>](#bool-lookupge-t-table-t-table-t-searchargument)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Searches the Table for the specified search argument.
| [LookupGE\<T, U\>](#bool-lookupge-t-u-table-t-table-t-searchargument-table-u-alttable)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html)) | Searches the Table for the specified search argument.
| [LookupGT\<T\>](#bool-lookupgt-t-table-t-table-t-searchargument)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Searches the Table for the specified search argument.
| [LookupGT\<T, U\>](#bool-lookupgt-t-u-table-t-table-t-searchargument-table-u-alttable)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html)) | Searches the Table for the specified search argument.
| [LookupLE\<T\>](#bool-lookuple-t-table-t-table-t-searchargument)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Searches the Table for the specified search argument.
| [LookupLE\<T, U\>](#bool-lookuple-t-u-table-t-table-t-searchargument-table-u-alttable)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html)) | Searches the Table for the specified search argument.
| [LookupLT\<T\>](#bool-lookuplt-t-table-t-table-t-searchargument)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Searches the Table for the specified search argument.
| [LookupLT\<T, U\>](#bool-lookuplt-t-u-table-t-table-t-searchargument-table-u-alttable)([Table\<T\>](/reference/runtime/qsys-runtime/table-1.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html)) | Searches the Table for the specified search argument.

### bool Lookup\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType searchType](/reference/runtime/qsys-runtime/search-type.html), [Indicator& ind](/reference/runtime/qsys-runtime/indicator.html))

Searches the Table for the specified search argument.

```cs
bool Lookup<T>(Table<T> table, T searchArgument, SearchType searchType, Indicator& ind)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [SearchType](/reference/runtime/qsys-runtime/search-type.html) | searchType | The type of lookup being performed.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | ind | Indicator which will be set on ('1') if the specified SearchType type is satisfied by the search.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if lookup is successful, false otherwise.

### bool Lookup\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType searchType](/reference/runtime/qsys-runtime/search-type.html), [Indicator& hiLoInd](/reference/runtime/qsys-runtime/indicator.html), [Indicator& eqInd](/reference/runtime/qsys-runtime/indicator.html))

Searches the Table for the specified search argument.

```cs
bool Lookup<T>(Table<T> table, T searchArgument, SearchType searchType, Indicator& hiLoInd, Indicator& eqInd)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [SearchType](/reference/runtime/qsys-runtime/search-type.html) | searchType | The type of lookup being performed.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | hiLoInd | Indicator which will be set on ('1') if the specified LookupStatus type is satisfied by the search.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | eqInd | Indicator which will be set on ('1') if Lookup finds an exact match within the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if lookup is successful, false otherwise.

### bool Lookup\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Searches the Table for the specified search argument.

```cs
bool Lookup<T>(Table<T> table, T searchArgument)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if an exact match is found, false otherwise.

### bool Lookup\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType searchType](/reference/runtime/qsys-runtime/search-type.html), [Table\<U\> result](/reference/runtime/qsys-runtime/table-1.html), [Indicator& ind](/reference/runtime/qsys-runtime/indicator.html))

Searches the Table for the specified search argument.

```cs
bool Lookup<T, U>(Table<T> table, T searchArgument, SearchType searchType, Table<U> result, Indicator& ind)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [SearchType](/reference/runtime/qsys-runtime/search-type.html) | searchType | The type of lookup being performed.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | result | If the Lookup is successful, the CurrentElement of the result table will be set to the index of the searched table's CurrentElement.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | ind | Indicator which will be set on ('1') if the specified SearchType type is satisfied by the search.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if lookup is successful, false otherwise.

### bool Lookup\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [SearchType searchType](/reference/runtime/qsys-runtime/search-type.html), [Table\<U\> result](/reference/runtime/qsys-runtime/table-1.html), [Indicator& hiLoInd](/reference/runtime/qsys-runtime/indicator.html), [Indicator& eqInd](/reference/runtime/qsys-runtime/indicator.html))

Searches the Table for the specified search argument.

```cs
bool Lookup<T, U>(Table<T> table, T searchArgument, SearchType searchType, Table<U> result, Indicator& hiLoInd, Indicator& eqInd)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [SearchType](/reference/runtime/qsys-runtime/search-type.html) | searchType | The type of lookup being performed.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | result | If the Lookup is successful, the CurrentElement of the result table will be set to the index of the searched table's CurrentElement.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | hiLoInd | Indicator which will be set on ('1') if the specified SearchType type is satisfied by the search.
| [Indicator&](/reference/runtime/qsys-runtime/indicator.html) | eqInd | Indicator which will be set on ('1') if Lookup finds an exact match within the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if lookup is successful, false otherwise.

### bool Lookup\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\> altTable](/reference/runtime/qsys-runtime/table-1.html))

Searches the Table for the specified search argument.

```cs
bool Lookup<T, U>(Table<T> table, T searchArgument, Table<U> altTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | altTable | If the Lookup is successful, the CurrentElement of the altTable table will be set to the index of the searched table's CurrentElement.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if an exact match is found, false otherwise.

### bool LookupGE\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Searches the Table for the specified search argument.

```cs
bool LookupGE<T>(Table<T> table, T searchArgument)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value greater than or equal to the searchArgument is found, false otherwise.

### bool LookupGE\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\> altTable](/reference/runtime/qsys-runtime/table-1.html))

Searches the Table for the specified search argument.

```cs
bool LookupGE<T, U>(Table<T> table, T searchArgument, Table<U> altTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | altTable | If the Lookup is successful, the CurrentElement of the altTable table will be set to the index of the searched table's CurrentElement.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value greater than or equal to the searchArgument is found, false otherwise.

### bool LookupGT\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Searches the Table for the specified search argument.

```cs
bool LookupGT<T>(Table<T> table, T searchArgument)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value greater than the searchArgument is found, false otherwise.

### bool LookupGT\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\> altTable](/reference/runtime/qsys-runtime/table-1.html))

Searches the Table for the specified search argument.

```cs
bool LookupGT<T, U>(Table<T> table, T searchArgument, Table<U> altTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | altTable | If the Lookup is successful, the CurrentElement of the altTable table will be set to the index of the searched table's CurrentElement.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value greater than the searchArgument is found, false otherwise.

### bool LookupLE\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Searches the Table for the specified search argument.

```cs
bool LookupLE<T>(Table<T> table, T searchArgument)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value less than or equal to the searchArgument is found, false otherwise.

### bool LookupLE\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\> altTable](/reference/runtime/qsys-runtime/table-1.html))

Searches the Table for the specified search argument.

```cs
bool LookupLE<T, U>(Table<T> table, T searchArgument, Table<U> altTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | altTable | If the Lookup is successful, the CurrentElement of the altTable table will be set to the index of the searched table's CurrentElement.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value less than or equal to the searchArgument is found, false otherwise.

### bool LookupLT\<T\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Searches the Table for the specified search argument.

```cs
bool LookupLT<T>(Table<T> table, T searchArgument)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value less than the searchArgument is found, false otherwise.

### bool LookupLT\<T, U\>([Table\<T\> table](/reference/runtime/qsys-runtime/table-1.html), [T searchArgument](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0), [Table\<U\> altTable](/reference/runtime/qsys-runtime/table-1.html))

Searches the Table for the specified search argument.

```cs
bool LookupLT<T, U>(Table<T> table, T searchArgument, Table<U> altTable)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | table | The table to search.
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | searchArgument | The element value being searched for in the array.
| [Table\<U\>](/reference/runtime/qsys-runtime/table-1.html) | altTable | If the Lookup is successful, the CurrentElement of the altTable table will be set to the index of the searched table's CurrentElement.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Returns true if a value less than the searchArgument is found, false otherwise.
