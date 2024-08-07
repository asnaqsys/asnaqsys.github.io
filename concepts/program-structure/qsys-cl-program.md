---
title: "Mastering QSYS CL Programs"
description: "Dive into QSYS CL programs with our guide. Learn to create, manage, and optimize CL programs effectively for your projects."
---

IBM i Command Language uses free-format syntax, similar to modern programming languages such as C#.

[ASNA Monarch Cocoon](https://docs.asna.com/documentation/Help150/Main_Monarch_90.htm) migrates CL Programs as classes derived from `QSys CLProgram` which is a specialized version of [QSys Program](/concepts/program-structure/qsys-program.html)

CL Program extends `QSys Program` by adding support for: 
1. %Switch, *BCAT, *TCAT methods.
2. Retrieve Job Attribute methods.
3. Data-Area operation methods.
4. File and Member (Add, Delete, Remove, Initialize, retrieve Member Description) methods.
5. Library-list (Add, Remove) methods.
6. File Override methods.
7. Delay/Resume Job methods.
8. Server Date Conversion methods.

## Notes: 
1. CL Programs do not have an [implicit logic cycle](https://www.ibm.com/docs/en/i/7.2?topic=cycle-rpg-other-implicit-logic).
2. CL Programs are de-activated when program completes. [For information about Program Activation read this](/concepts/program-structure/qsys-program.html). 