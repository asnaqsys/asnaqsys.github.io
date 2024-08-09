---
title: "DynamicCaller class           | QSYS API Reference Guide"
description: "Support for CALLD as a dynamic call. "
last_modified_at: 2024-08-09T17:25:29Z
---

Support for CALLD as a dynamic call.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DynamicCaller](#dynamiccallericaller)([ICaller](/reference/runtime/qsys-runtime/i-caller.html)) | Dynamic caller constructor.

### DynamicCaller([ICaller](/reference/runtime/qsys-runtime/i-caller.html))

Dynamic caller constructor.

```cs
DynamicCaller(ICaller)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | caller | The caller object in the dynamic call.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ICaller](/reference/runtime/qsys-runtime/i-caller.html) | Caller | The caller object in the dynamic call. |

## Methods

| Signature | Description |
| --- | --- |
| [FindTypeInAssemblyList](#type-findtypeinassemblyliststring-classname-assembly-callerassembly)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Assembly](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.assembly?view=net-8.0)) | Looks for a program in the assemblies of the Process AssemblyList
| [GetMetaObject](#dynamicmetaobject-getmetaobjectexpression-parameter)([Expression](https://learn.microsoft.com/en-us/dotnet/api/system.linq.expressions.expression?view=net-8.0)) | Defines the object that supports CallD.
| [ProgramExists](#bool-programexistsstring-programname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines if a program exists in the given assembly lists.
| [SetDynamicAssemblyList](#void-setdynamicassemblyliststring-assemblies)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates the list of assemblies representing dynamic references. CALLD targets will be searched for in this list.

### Type FindTypeInAssemblyList([string className](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Assembly callerAssembly](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.assembly?view=net-8.0))

Looks for a program in the assemblies of the Process AssemblyList

```cs
Type FindTypeInAssemblyList(string className, Assembly callerAssembly)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | className | The class name of the program.
| [Assembly](https://learn.microsoft.com/en-us/dotnet/api/system.reflection.assembly?view=net-8.0) | callerAssembly | The assembly of the caller. Use null to not search in the caller assembly.

#### Returns

| Type | Description
| --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | The type of the program.

### DynamicMetaObject GetMetaObject([Expression parameter](https://learn.microsoft.com/en-us/dotnet/api/system.linq.expressions.expression?view=net-8.0))

Defines the object that supports CallD.

```cs
DynamicMetaObject GetMetaObject(Expression parameter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Expression](https://learn.microsoft.com/en-us/dotnet/api/system.linq.expressions.expression?view=net-8.0) | parameter | The expression representing the DynamicMetaObject during the dynamic bunding process.

#### Returns

| Type | Description
| --- | ---
| [DynamicMetaObject](https://learn.microsoft.com/en-us/dotnet/api/system.dynamic.dynamicmetaobject?view=net-8.0) | The CallDMetaCaller object to use for the dynamic call.

### bool ProgramExists([string programName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines if a program exists in the given assembly lists.

```cs
bool ProgramExists(string programName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programName | Name of the program. Can be a simple name or fully qualified with its namespace.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if program found, otherwise false.

### void SetDynamicAssemblyList([string assemblies](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates the list of assemblies representing dynamic references. CALLD targets will be searched for in this list.

```cs
void SetDynamicAssemblyList(string assemblies)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | assemblies | Comma separated list of assemblies or patterns.
