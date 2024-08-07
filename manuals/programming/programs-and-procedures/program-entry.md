---
title: "Program Entry Points: A Comprehensive Guide"
description: "Learn about program entry points, their importance in software development, and how to effectively manage them for optimal program execution."
---

A [Monarch Program](/concepts/architecture/monarch-programs.html) migrated from the IBM i should have the ability to be called by other programs providing similar semantics to the original call/return facilities as well as respecting the expectation of the program's instantiation in an [Activation Group](/concepts/architecture/activation-groups.html).

When a program calls another program, all it needs to know is the program's name, i.e.: the programs class name.  The calling program may even provide the name to the call facility by passing a string variable with the called program's name.

In order to pass control to the method with the main body of the called program, two C# helper methods are created to facilitate creating or finding the proper instance of the program and managing the parameter passing:
 * A static ```_ENTRY``` method and
 * An instance ```__ENTRY``` method

 The main body of the program, derived from the main C-Specs, is an instance method called StarEntry.

## Static _ENTRY Method
The static ```_ENTRY``` method is the initial target of a program call. This method is responsible for the following tasks:
 * Find the instance of the program in its Activation Group, if it does not exist, then create the instance.
 * Call the instance method ```__ENTRY```
 * After retuning from the __ENTRY call, removes the program invocation stack entry, and if needed deactivates the program by removing it from the Activation Group.
 * If the parameters to _ENTRY are passed by reference, they need to be copied into local fields and restored from the local fields upon returning to the caller. 


## Instance __ENTRY Method

The instance ```__ENTRY``` method takes care of maintaining the semantics of the initialization:
 * Copies the parameters passed to the program to the global fields where the rest of the program expects to find them.
 * Counts the actual number of parameters passed to the program.
 * Calls the initialization routine (called PROCESS_STAR_INZSR).
 * Calls the main procedure StarEntry wrapping the call in a try/catch block to enable it to process benignly the exception generated by the ```Return``` operation.
 * After returning from the StarEntry call, copies the values in the global fields back to those parameters that were passed by reference.

## StarEntry Method
The  main body of the program, derived from the main C-Specs, is located in an instance method named ```StarEntry```.  This method contain user code.
