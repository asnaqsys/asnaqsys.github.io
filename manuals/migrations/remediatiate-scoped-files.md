---
title: "Remediation of Procedure Scoped Files"
description: "Strategies and best practices for the remediation of Procedure-Scoped files."
---

## Remediation

There are three strategies to remediate the lack of support for procedure scoped files in AVR:
 + Make DclXxxxFile Global
 + Create a Nested Class for the Procedure
 + Create a Separate Class for the Procedure

### Make DclXxxxFile Global
If the File definition does not interfere in name, format name or field names, then the simplest remediation is to pull the DclXxxxFile to outer scope.  Care will have to be taken to potentially open/close the file when the procedure is invoked/returns. 

Even if there are name collisions, this strategy may still be used by renaming the file, format or fields (via prefix) and then adjusting the names used in the procedure.

### Create a Nested Class for the Procedure
If there is too much collision of names, or if the globalization of the file offends the sensibility of the customer’s developers, then the remediation includes the creation of a new class.  The new class will encompass be the File and the Procedure.  

Under this strategy, the new class becomes a child class of the original class.  The original class will have a Procedure proxy which will forward the calls to the child class.  The original class will need a private field to hold the instance of the child class; instantiation can occur in the constructor of the original class or in the Procedure proxy.

The child class will need a reference to the original class instance in order for the child to have access to the original class’ members; this instance can be set at child construction time.  

It may also be necessary to provide the original class with helper methods that the child can call.  For instance, say the Procedure wanted to read in the LDA, but the LDA fields are defined at the original class level.  Then the Procedure could call back a helper method in the original class, via the instance given at construction, to do the reading and populating the original fields.  After that, the Procedure could then use the parent’s instance to access the outer fields with the data just read.

### Create a Separate Class for the Procedure
The big advantage of using a nested class versus having the Procedure’s class be a sibling of the original class is that the child can access private members of the original class.

Now, if the Procedure does not access any data from the Original class, then it may be better to create a separate class altogether. 

There may still be a need for a proxy Procedure in the original class.

## Locating Files in Procedures
To find instances of files declared within procedures, search for some commands using this regular expression:

>  ```(BegProc|EndProc|DclDiskFile|DclWorkStnFile)```

Swap around the result in each line such that the command comes first (transfer the source name and line number to the end of the line). Then look into the modified set of lines for the offenders using this regular expression:

> ```BegProc *[A-Za-z@#$].*\r\n *Dcl```
