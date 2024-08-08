---
title: "ProgramEntryAttribute class   | QSYS API Reference Guide"
description: "A non-RPG class may use this attribute to indicate which method in it corresponds to RPG&#39;s *ENTRY. "
last_modified_at: 2024-08-08T21:41:46Z
---

A non-RPG class may use this attribute to indicate which method in it corresponds to RPG's *ENTRY.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ProgramEntryAttribute](#programentryattributestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a ProgramEntryAttribute object.

### ProgramEntryAttribute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a ProgramEntryAttribute object.

```cs
ProgramEntryAttribute(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | entryProcedureName | Name of *ENTRY in this class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | EntryProcedureName | Gets the name of *ENTRY in this class. |
