---
title: "Migrating Record Locking/Unlocking to MSSQL: Best Practices"
description: "This document provides a detailed guide on migrating record locking and unlocking mechanisms from legacy systems to SQL Server."
---

## Overview

Although DGL tries to make _SQL Server_ look like DB2 for IBM i, for some operations record locking behaves differently under DGL.

The record locking problem arises in three areas: 
 1. The `Unlock` operation loses the 'current' position.
 2. The `Update` operation keeps the record locked.
 3. There is no support for the  `Access(*NoLock)` keyword on read operations (CHAIN, READ, READP, READE, READPE).

## Some background on record locking

### DataGate for IBM i

DG/400 determines the type and duration of record locks depending on how the file is opened.

 - For read-only files, when a record is read, there is no lock requested on it. Even if some other application has the record lock, the reading application does not block on the lock, that is, the record is read in spite of being locked by somebody else (a _dirty_ read is performed).

 - For files open for update, every time a record is read it is write-locked so that other updating applications cannot read it. The write lock is held until the record is updated or explicitly unlocked by the application or when the program uses the file to position or read another record. <br/>Additionally for files opened for update, the read op-codes have an option `Access(*NoLock)`[^1] to avoid locking the record.

### DataGate Linear for SQL Server

DGL (using server cursors) also determines the locking characteristics based on how the file is opened.

 - For read-only files, DGL behaves like DG/400, that is, locks are neither placed nor considered on records being read.

 - The behavior of DGL when the file is opened for update is similar to DG/400 but with two significant **differences**:
    1. Update Operation: Updating a record **does not** release the lock on the record.
    2. Unlock Opeartion: Explicitly unlocking a record causes the 'current record position' to be **lost**, meaning you can not perform a subsequent sequential read (next/previous) without repositioning the file with a SET (SETLL/SETGT) or CHAIN.

## Read - Update/Unlock Sequences

**In a Loop**
Tight loops involving an initial `Chain/SetLL/SetGT` operation followed by  sequential reads (`Read/ReadP/ReadE/ReadPE`) with either Update/Unlock opearations in the loop can have the Unlock opearation removed from the loop. If the reads were done via `Read/ReadP` within the loop, then add an `Unlock` at the end of the loop. Alternatively, the loop could be converted to use Range operations.

**Out of a Loop**
The most demanding change is the one requiring segments of code involving `CHAIN-UPDATE`.  Combinations have to be studied and possibly modified. 

* If the `CHAIN-UPDATE` happens in a tight loop, then at the end of the loop an `UNLOCK` should be issued to release the last record updated. Note however that the record position will be lost after the `UNLOCK`.
* If the `CHAIN-UPDATE` is sprinkled throughout the code, then each case has to be closely studied to see if the current position is used in a subsequent read operation.

## Access(*NoLock) Option on Reads

> DataGate can communicate **directly** with SQL Server using ADO.NET; this method of communication is known as _DataGate Linear_. To use _DataGate Linear_ set the ([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)`.PlatformAttribute = "*SQLCLIENT"`.

Starting with version 5.0, _DataGate Linear_ supports reading records without locking them on files that were open for `update`. To request a read with no lock, add the keyword `Access(*NoLock)`[^1] to the read/chain operation.

While this feature is supported on DataGate for IBM i, it  was not available on SQL Server when it was accesed via DataGate. On those older versions, whenever a file was accessed for `update`, any read would always apply a lock to the record read. Now with _DataGate Linear_ it is possible to pass the parameter requesting the record not be locked. Notice that  _DataGate for SQL Server_ (DSS) does not have this enhancement.

The _DataGate Linear_ feature comes with a restriction however.  It is not possible to switch between **sequential** reads with-lock and without-lock. In order to switch modes, a random-access operation is needed between the reads, this operation could be a seek (SETLL) or random-read (CHAIN).


----

[^1]: Do not confuse the Visual RPG and Encore RPG keyword option `Access(*NoLock)` with the SQL Server deprecated hint `NOLOCK`.