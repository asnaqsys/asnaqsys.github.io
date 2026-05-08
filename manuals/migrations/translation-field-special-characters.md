---
title: "Translation of Special Characters in Field Names"
description: "Learn to manage special characters in translation fields effectively. This guide offers insights and best practices for accurate translations."
---

The valid characters in RPG and DDS include some special characters that have to be translated when migrating to .NET.

These are the replacement tables for each case.

## Display Files

| DDS Field Original Character | Razor Page Replacement Character |
| ---------------------------- | ---------------------------------|
| @ | a 
| #	| h 
| $	| s
| § | c
| € | e
| £ | p
| ¥ | y 

There is no possibility of conflict because DDS fields are all uppercase.

## Database and Printer Files
Field names retain their original names, including special characters.

## CL Programs

| CL Field Original Character | C# Replacement Character |
| --------------------------- | -------------------------|
| & | _


There is no possibility of conflict as all fields in CL have the leading &.

## RPG & CL Programs

| Program Field Original Character | C# Replacement Character |
| -------------------------------- | ---------------------------------|
| @ | a 
| #	| h 
| $	| s
| § | c
| € | e
| £ | p
| ¥ | y

Possibility of conflict is low due to C# being case sensitive and many original field names are uppercase. 

Conflicts will be detected when the compiler finds the double definition and the migrator will have to resolve it manually by renaming one of the two fields and updating all references to it by looking at the original RPG code. 

