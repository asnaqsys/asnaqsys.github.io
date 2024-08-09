---
title: "StringOps class               | QSYS API Reference Guide"
description: "Provide fixed length character string storage and operations. "
last_modified_at: 2024-08-09T16:18:25Z
---

Provide fixed length character string storage and operations.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [Adjust](#string-adjuststring-source-int-targetlength-bool-padleft)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Adjust the length of a string to a given value, by padding or truncating the string.
| [AdjustLeftLength](#string-adjustleftlengthstring-source-int-targetlength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjust the length of a string to a given value, by padding or truncating the string on the left.
| [AdjustRightLength](#string-adjustrightlengthstring-source-int-targetlength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adjust the length of a string to a given value, by padding or truncating the string on the right.
| [GetArrayChars](#void-getarraycharsarray-array-char--target-int-targetindex-int-charlength)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy characters from strings stored in an array to a char[].
| [GetArrayOneChars](#void-getarrayonecharsarray-array-char--target-int-targetindex)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy characters from an array to a one-dimensional array.
| [GetChars](#void-getcharsstring-source-char--destination-int-destinationindex-int-destinationlength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy characters from a string to an array of char.
| [GetIndices](#int32--getindicesarray-myarr-int-i)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Get the indices of a multidimensional array for the given position.
| [MergeLeftString](#string-mergeleftstringstring-sourcevalue-string-targetvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's MoveLeft. Merge the sourceValue into targetValue starting at position 0.
| [MergeRightString](#string-mergerightstringstring-sourcevalue-string-targetvalue)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | RPG's Move(Right). Merge the sourceValue into targetValue starting at the end of targetValue.
| [SetArrayChars](#void-setarraycharsarray-array-char--source-int-sourceindex-int-charlength)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Load an array of strings with the strings constructed out of a char[].
| [SetArrayOneChars](#void-setarrayonecharsarray-array-char--source-int-sourceindex)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy characters from a one-dimensional array to an array.
| [SetChars](#string-setcharsstring-destination-char--source-int-sourceindex-int-sourcelength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Create a string out of character in a char[].
| [SetLengthOfField](#void-setlengthoffieldstring-source-int32-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Sets the length parameter to the length of the string. Throws an exception if the string is null.
| [SetVaryingLengthChar](#string-setvaryinglengthcharstring-source-int-maxlength-int32-length)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Keep a string with at most maxLength characters, and compute its current length.
| [TestNumeric](#testnumericresult-testnumericstring-candidate)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Test a string for any of the conditions specified in the TestNumericResult enumeration.
| [VaryLength](#string-varylengthint-length-string-source-int-maxlength-int32-newlength)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Set the length of source to the given length subject to maxLength, and return the newLength.

### string Adjust([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool padLeft](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Adjust the length of a string to a given value, by padding or truncating the string.

```cs
string Adjust(string source, int targetLength, bool padLeft)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetLength | The desired length.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | padLeft | True to pad/truncate on the left, false to pad/truncate on the right.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### string AdjustLeftLength([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjust the length of a string to a given value, by padding or truncating the string on the left.

```cs
string AdjustLeftLength(string source, int targetLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetLength | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### string AdjustRightLength([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int targetLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adjust the length of a string to a given value, by padding or truncating the string on the right.

```cs
string AdjustRightLength(string source, int targetLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to adjust.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetLength | The desired length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string at the desired length.

### void GetArrayChars([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] target](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int targetIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int charLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy characters from strings stored in an array to a char[].

```cs
void GetArrayChars(Array array, Char[] target, int targetIndex, int charLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The source of the operation.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | target | The target char[].
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetIndex | Position in target where the copying should start.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | charLength | Length of the strings in the source array.

### void GetArrayOneChars([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] target](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int targetIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy characters from an array to a one-dimensional array.

```cs
void GetArrayOneChars(Array array, Char[] target, int targetIndex)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The source of the operation.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | target | The target char[].
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetIndex | Position in target where the copying should start.

### void GetChars([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] destination](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int destinationIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int destinationLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy characters from a string to an array of char.

```cs
void GetChars(string source, Char[] destination, int destinationIndex, int destinationLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | destination | The char[] into which to copy source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | destinationIndex | The starting position on the destination array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | destinationLength | How many characters to copy.

### Int32\[\] GetIndices([Array myArr](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int i](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Get the indices of a multidimensional array for the given position.

```cs
Int32[] GetIndices(Array myArr, int i)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | myArr | The multidimensional array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | i | The position of the element.

#### Returns

| Type | Description
| --- | ---
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | An in[] with the indices of the i-th element.

### string MergeLeftString([string sourceValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's MoveLeft. Merge the sourceValue into targetValue starting at position 0.

```cs
string MergeLeftString(string sourceValue, string targetValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sourceValue | Source value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetValue | Target value.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The result of the merge.

### string MergeRightString([string sourceValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string targetValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

RPG's Move(Right). Merge the sourceValue into targetValue starting at the end of targetValue.

```cs
string MergeRightString(string sourceValue, string targetValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sourceValue | Source value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetValue | Target value.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The result of the merge.

### void SetArrayChars([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int sourceIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int charLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Load an array of strings with the strings constructed out of a char[].

```cs
void SetArrayChars(Array array, Char[] source, int sourceIndex, int charLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | Array of strings to load.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | source | The char[] that's the source of the strings.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceIndex | Position in source where to start constructing strings.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | charLength | Length of the individual strings to be constructed.

### void SetArrayOneChars([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int sourceIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy characters from a one-dimensional array to an array.

```cs
void SetArrayOneChars(Array array, Char[] source, int sourceIndex)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The destination of the copy.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | source | The source char[].
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceIndex | Position in source where to start copying chars.

### string SetChars([string destination](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int sourceIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int sourceLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Create a string out of character in a char[].

```cs
string SetChars(string destination, Char[] source, int sourceIndex, int sourceLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | destination | String that serves as model for the created string.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | source | The char[].
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceIndex | The starting position in the array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceLength | The length of the array.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string created with characters from the array.

### void SetLengthOfField([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Int32& length](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Sets the length parameter to the length of the string. Throws an exception if the string is null.

```cs
void SetLengthOfField(string source, Int32& length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The resulting value of the length of the string.

### string SetVaryingLengthChar([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int maxLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Int32& length](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Keep a string with at most maxLength characters, and compute its current length.

```cs
string SetVaryingLengthChar(string source, int maxLength, Int32& length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to analyze.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxLength | The maximum allowed length for source.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The resulting length of source.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of source adjusted to maxLength if needed.

### TestNumericResult TestNumeric([string candidate](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Test a string for any of the conditions specified in the TestNumericResult enumeration.

```cs
TestNumericResult TestNumeric(string candidate)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | candidate | The string to test.

#### Returns

| Type | Description
| --- | ---
| [TestNumericResult](/reference/runtime/qsys-runtime/test-numeric-result.html) | A TestNumericResult value specifying the status of the string.

### string VaryLength([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int maxLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Int32& newLength](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Set the length of source to the given length subject to maxLength, and return the newLength.

```cs
string VaryLength(int length, string source, int maxLength, Int32& newLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Desired length of source.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to adjust in length.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxLength | The maximum allowed length.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | newLength | The resulting length.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of source adjusted to the given length.
