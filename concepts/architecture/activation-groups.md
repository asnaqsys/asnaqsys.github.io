---
title: "Understanding Activation Groups"
description: "Learn about Activation Groups and their role in system performance and organization. A concise guide for developers."
---

An Activation Group is a substructure of a Job that serves to control the state of groups of programs. The Activation Group keeps a reference for each program that belongs to it.

Before a program is given execution control, the program’s activation instance has to be found or created; if an adequate activation exists in the Job it is used, otherwise, the program must be activated first.

When a program is activated, its variables are allocated in memory and some  other one-time initialization code may run. Related programs are activated in activation groups. Activation groups associate the state of related programs.

When a program ends execution and before returning to the caller, the program may be deactivated depending on how the program ended and the characteristics of its activation group.

## Program Activation
When a program is called for the first time an instances to the program's class has to be created. A subsequent call to the program may reuse the program's instance or it may create a new instance for that call.

Programs and Service Programs are marked with an attribute that specify the activation group where they belong. There are three general possibilities for this attribute. A program may be marked with an activation group attribute to:
  * Be associated with a particular named activation group (```ActivationGroup("SomeName")```).
  * Have a brand new activation group created and be associated with it (```NewActivationGroup```).
  * Associate with the activation group of the program that called it (```CallerActivationGroup```).

## Activation Group Creation
Named Activation groups are created when the first program that belongs to it gets activated. 

When programs marked with the ```NewActivationGroup``` are called, an activation group is created with a system generated name. As described below, the activation group will be deleted when the program returns to its caller.

When a Job starts, it creates an activation group named <b>*DFTACTGRP</b> that is used by default for programs that are not marked with an activation group attribute, typically OPM programs.

## Program Deactivation
A program gets *deactivated* or disposed when its Activation Group is deleted.

When a programs gets deactivated, its Dispose method gets called. The  implementation of the Dispose of the program base class calls Dispose on each of the Modules in the program's module collection.

## Deleting an Activation Group
There are three ways for an Activation Group to be deleted:
  * After a program marked with the ```NewActivationGroup``` completes its execution and is returning to the calling program.
  * Named activations groups can be deleted by calling the Module method ```JobServices.ReclaimActivationGroup```.
  * When the job reaches its natural end, it deletes all surviving activation groups including <b>*DFTACTGRP</b>.
