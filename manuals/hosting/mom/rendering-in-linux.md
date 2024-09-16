---
title: "Rendering a Report in Linux and Elsewhere."
description: "Describes how to render a Manuscript without the support of Windows in environments like Linux."
---

This document discusses a Manuscript Renderer which does not use the support of Windows and can be used in environments like Linux. 

## Render without Windows
A general rendering process reads a Manuscript and instantiates the print controls according to their design time properties and then iterates over the pages of the report setting the recorded runtime property values and calling the paint facilities of the controls. As described in the [introduction to Printer Files](/concepts/printing/printer-files.html), Printer Files are composed of .NET Framework Windows Forms Controls and these are non-functional on non-Windows environments.  In order to render a Manuscript in these environments, it is necessary to replace the painting capabilites of the Controls that use the Windows GDI+ facilities.  This can be achieved by producing replacements of the ASNA Print Controls and any other Windows or Third Party controls used to create the Printer File/Manuscript. 

## ASNA.QSys.Renderer.PDFOnly
ASNA provides an implementation of a report Renderer that creates a PDF document utilizing the open-source [PDFsharp Library](https://docs.pdfsharp.net/PDFsharp/Overview/About.html), this Renderer is called `ASNA.QSys.Renderer.PDFOnly`

The `ASNA.QSys.Renderer.PDFOnly` implements Control replacements which instead of painting onto a Windows canvas, they 'paint' to a PDF document.  

It is your responsibilty to build and install `ASNA.QSys.Renderer.PDFOnly` on your system. You can find the projects' sources in the [GitHub Repository](//github.com/asnaqsys/ASNA.QSys.Renderer).


## ASNA.QSys.Renderer.PDFOnly Control Replacements
The print control classes source is part of the `ASNA.QSys.Renderer.PDFOnly` project. `ASNA.QSys.Renderer.PDFOnly` and its control replacements rely on the [PDFsharp Library](https://docs.pdfsharp.net/PDFsharp/Overview/About.html) which is included via its [NuGet Package](//www.nuget.org/packages/PDFsharp).

The control replacement provided include those from DataGate and few from Windows.  These are:
 - ASNA Print Control Replacements:
   + AutoField - Prints an Attribute of the report: Computer Name, Page Number or Count, Creation date/time, Process date/time.
   + CharField - Prints a fixed length character field.
   + DecField - Prints a fixed length Binary, Packed or Zoned decimal field.
   + DateTimeField - Prints a Date, Time or Timestamp field.   
   + Label - Prints a Constant character string.
   + Line - Prints a staight Line.
   + Shape - Prints a Rectange, Square, Oval or Circle.
- Selected Windows Control Replacements:
   + CheckBox - Prints a possibly checked box.
   + PictureBox - Prints an image with a format of: PNG, JPEG or BMP.

The minimum implementation is provided for the controls in order to produce their 'print' rendering. If there is additional functionality needed you can add the to the implementation source.