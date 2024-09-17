---
title: "Rendering a Report in Windows."
description: "Describes how to render a Manuscript in a environment hosted by a Windows operating system."
---

This document discusses how to render a Manuscript with the support of Windows. ASNA provides two different implementations of a Report Renderer:
 + [DataGate Renderer](#datagate-renderer)
 + [ASNA.QSys.Renderer.WindowsOnly](#asnaqsysrendererwindowsonly)

## Common Features of the Two Implementations

A [Printer File](/concepts/printing/printer-files.html) is a collection of [Windows Forms Controls](//learn.microsoft.com/en-us/dotnet/desktop/winforms/controls/overview).  ASNA provides a set of these controls (distributed in the **ASNA.DataGate.PrintControls.dll** assembly) which are well suited for printing, but other controls may be used when designing a Printer File. When a report is created using a Printer File, the Controls are not used, but their design and runtime property values are recorded in a Manuscript file. 

The Rendering process reads the Manuscript and instantiates the controls according to their design time properties and then iterates over the pages of the report setting the recorded runtime property values and rising the controls [OnPaint](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.control.onpaint)'s event. The Paint event receives the [System.Drawing.Graphics](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.graphics) instance that encapsulates the GDI+ drawings surface of the printer where the report is being renderer.

> The DataGate Renderer and the ASNA.QSys.Renderer.WindowsOnly programs are .NET Framework executables that depend on the Windows operating system.

The Printer where the report is created must be [installed](//support.microsoft.com/en-us/windows/install-a-printer-in-windows-cc0724cf-793e-3542-d1ff-727e4978638b) on the computer where the rendering is being executed and it can be a physical printer or the "Microsoft Print to PDF" printer.

Both implementations of the Renderer accept the same set of [command line options](/manuals/hosting/mom/manuscript-renderer.html#renderer-command-line-options)

## DataGate Renderer
The DataGate Renderer is installed as part of the ASNA DataGate® Studio product which can be [downloaded](https://www.asna.com/downloads/en) and installed directly. It is also included in several other ASNA product, most notablly [ASNA DataGate® WebPak](https://www.asna.com/downloads/en) and [ASNA Encore RPG™](https://www.asna.com/en/migration/encore).

The DataGate Renderer program is called simply `Renderer.exe` and is typically installed in the Program Files folder:<br/> 
&nbsp;&nbsp;&nbsp;`C:\Program Files\Common Files\ASNA Shared\Client\Common` 

In addition to the Renderer program, the installation places the assembly `ASNA.DataGate.PrintControls.dll` in the folder:<br/>
&nbsp;&nbsp;&nbsp; `C:\Program Files\Common Files\ASNA Shared\Client\xx.x` <br/>
(where xx.x is the version number of the product being installed) and registers the assembly in the [GAC](//learn.microsoft.com/en-us/dotnet/framework/app-domains/gac).


## ASNA.QSys.Renderer.WindowsOnly
The ASNA.QSys.Renderer.WindowsOnly can be used to print a Manuscript file to any printer installed on a **Windows computer**, including the 'Microsoft Print To PDF' printer.

`ASNA.QSys.Renderer.WindowsOnly` is the Open Source releas of the DataGate components. To distiguish this components from those ship with the standard DataGate ones the names have been modified.

It is your responsibilty to build and install these components on your system. You can find the project sources in the [GitHub Repository](//github.com/asnaqsys/ASNA.QSys.Renderer).



