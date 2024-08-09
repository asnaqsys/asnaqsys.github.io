---
title: "FixedArrayMethods class       | QSYS API Reference Guide"
description: "Contains extension methods for handling FixedArrays according to RPG semantics. "
last_modified_at: 2024-08-09T17:25:29Z
---

Contains extension methods for handling FixedArrays according to RPG semantics.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [FillArrayWith\<TDim, T\>](#void-fillarraywith-tdim-t-ifixedarraybase-tdim-t-targetarr-int-startposition-t-val)([IFixedArrayBase\<TDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Fills a given array with the specified object.
| [Initialize\<TDim, T\>](#void-initialize-tdim-t-ifixedarraybase-tdim-t-targetarr-t-val)([IFixedArrayBase\<TDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Initializes the elements of an arbitrary array to the same value.
| [MoveToArrayDiffFieldLength\<TSourceDim, TSource, TTargetDim, TTarget\>](#void-movetoarraydifffieldlength-tsourcedim-tsource-ttargetdim-ttarget-ifixedarraybase-tsourcedim-tsource-sourcearr-int-sourcestartat-ifixedarraybase-ttargetdim-ttarget-targetarr-int-targetstartat)([IFixedArrayBase\<TSourceDim, TSource\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, TTarget\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination array of different field lengths, no padding.
| [MoveToArrayDiffFieldLengthWithPad\<TSourceDim, TSource, TTargetDim, TTarget\>](#void-movetoarraydifffieldlengthwithpad-tsourcedim-tsource-ttargetdim-ttarget-ifixedarraybase-tsourcedim-tsource-sourcearr-int-sourcestartat-ifixedarraybase-ttargetdim-ttarget-targetarr-int-targetstartat)([IFixedArrayBase\<TSourceDim, TSource\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, TTarget\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination array of different field lengths, with padding.
| [MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarray-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination numeric array.
| [MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarray-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination numeric array.
| [MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarray-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination fixed decimal array.
| [MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarray-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source fixed decimal array to destination fixed decimal array.
| [MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarray-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source datetime array to destination numeric array.
| [MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarray-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source datetime array to destination fixed decimal array.
| [MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarraywithpad-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination numeric array, padding the result.
| [MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarraywithpad-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination numeric array, padding the result.
| [MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarraywithpad-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source array to destination fixed decimal array, padding the result.
| [MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarraywithpad-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source fixed decimal array to destination fixed decimal array, padding the result.
| [MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarraywithpad-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source datetime array to destination numeric array, padding the result.
| [MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>](#void-movetonumericarraywithpad-tsourcedim-ttargetdim-t-u-ifixedarraybase-tsourcedim-t-source-int-srcstartpos-ifixedarraybase-ttargetdim-u-target-int-dststartpos)([IFixedArrayBase\<TSourceDim, T\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IFixedArrayBase\<TTargetDim, U\>](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's MOVEA. Moves source datetime array to destination fixed decimal array, padding the result.

### void FillArrayWith\<TDim, T\>([IFixedArrayBase\<TDim, T\> targetArr](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int startPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [T val](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Fills a given array with the specified object.

```cs
void FillArrayWith<TDim, T>(IFixedArrayBase<TDim, T> targetArr, int startPosition, T val)
```

### void Initialize\<TDim, T\>([IFixedArrayBase\<TDim, T\> targetArr](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [T val](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Initializes the elements of an arbitrary array to the same value.

```cs
void Initialize<TDim, T>(IFixedArrayBase<TDim, T> targetArr, T val)
```

### void MoveToArrayDiffFieldLength\<TSourceDim, TSource, TTargetDim, TTarget\>([IFixedArrayBase\<TSourceDim, TSource\> sourceArr](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int sourceStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, TTarget\> targetArr](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination array of different field lengths, no padding.

```cs
void MoveToArrayDiffFieldLength<TSourceDim, TSource, TTargetDim, TTarget>(IFixedArrayBase<TSourceDim, TSource> sourceArr, int sourceStartAt, IFixedArrayBase<TTargetDim, TTarget> targetArr, int targetStartAt)
```

### void MoveToArrayDiffFieldLengthWithPad\<TSourceDim, TSource, TTargetDim, TTarget\>([IFixedArrayBase\<TSourceDim, TSource\> sourceArr](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int sourceStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, TTarget\> targetArr](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination array of different field lengths, with padding.

```cs
void MoveToArrayDiffFieldLengthWithPad<TSourceDim, TSource, TTargetDim, TTarget>(IFixedArrayBase<TSourceDim, TSource> sourceArr, int sourceStartAt, IFixedArrayBase<TTargetDim, TTarget> targetArr, int targetStartAt)
```

### void MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination numeric array.

```cs
void MoveToNumericArray<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination numeric array.

```cs
void MoveToNumericArray<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination fixed decimal array.

```cs
void MoveToNumericArray<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source fixed decimal array to destination fixed decimal array.

```cs
void MoveToNumericArray<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source datetime array to destination numeric array.

```cs
void MoveToNumericArray<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArray\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source datetime array to destination fixed decimal array.

```cs
void MoveToNumericArray<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination numeric array, padding the result.

```cs
void MoveToNumericArrayWithPad<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination numeric array, padding the result.

```cs
void MoveToNumericArrayWithPad<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source array to destination fixed decimal array, padding the result.

```cs
void MoveToNumericArrayWithPad<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source fixed decimal array to destination fixed decimal array, padding the result.

```cs
void MoveToNumericArrayWithPad<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source datetime array to destination numeric array, padding the result.

```cs
void MoveToNumericArrayWithPad<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```

### void MoveToNumericArrayWithPad\<TSourceDim, TTargetDim, T, U\>([IFixedArrayBase\<TSourceDim, T\> source](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int srcStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IFixedArrayBase\<TTargetDim, U\> target](/reference/runtime/qsys-runtime/i-fixed-array-base-2.html), [int dstStartPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's MOVEA. Moves source datetime array to destination fixed decimal array, padding the result.

```cs
void MoveToNumericArrayWithPad<TSourceDim, TTargetDim, T, U>(IFixedArrayBase<TSourceDim, T> source, int srcStartPos, IFixedArrayBase<TTargetDim, U> target, int dstStartPos)
```
