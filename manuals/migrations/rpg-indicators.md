---
title: "Migrating Indicators"
description: "Comprehensive overview of migrating RPG indicators to modern programming paradigms, replacement and mapping to new constructs"
---

## RPG Arrays vs C# Arrays
In RPG on the IBM i all array elements are numbered starting at 1.  

In C# and other .NET languages like ASNA Encore RPG (ECR) array elements are numbered starting at 0.  An RPG program migrated to C# reflects this difference and it is normal to see array operations using an index decremented by one from the original RPG sources.  

### The *IN array
There is one concession/exception in ECR for the *IN indicator array.  In an effort to maintain sanity for Encore RPG developers, the *IN (or _IN) array is 100 positions long with the first position left unused.  This was done so that in ECR the following statement would always hold true:

` *IN07 ≡ *IN[07]`

## Data structure Member Offsets
Similar to arrays, there is a difference in the implementations of data structures.  In IBM i’s RPG, data structure element **positions** begin at byte 1. In the ASNA runtime for C#, the member **offsets** begin at 0. Migrated code will reflect this difference in the definition of the data structures in C#.

## RPG’s INDDS – Indicator Data Structure
When a data structure is used in lieu of the *IN array to communicate with a device file (workstation or print file) this is specified in RPG via the INDDS keyword (INDicator Data Structure).  INDDS should point to a data structure that must contain 99 indicators. Due to the way data structure offset are specified in C# (starting at 0), the data structure **offsets** to individual indicators will be one number smaller than the **indicator number** used by the device file definition.  
