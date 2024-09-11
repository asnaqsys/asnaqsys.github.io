---
title: "Renderers Available to Create PDFs or Paper Reports"
description: "Explore how to use the Manuscript Renderer for outputing to a printer, including the command line options."
---

The final phase in the process of creating a report is the rendering of the manuscript. A renderer sends the formated contents of a manuscript to a printer or a PDF file. DataGate provides a default renderer program (Renderer.exe) which yields a printout produced to a Windows installed printer. The Renderer can be executed automatically when a Printer File is closed or be invoked by an operator or application. There are command options that can be set to control certain aspects of the rendering operation when Renderer.exe is executed from the Command Line.

You can read the [Concepts behind printing here](/concepts/printing/printing-introduction.html) and the [Printer Files concepts here](/concepts/printing/printer-files.html).

## Three Renderers
In addition to the DataGate Renderer, there are two open source renderers that can be used without having to install DataGate on the rendering machine. ASNA provides these three renderers:
 1. DataGate Renderer
 2. Open.Renderer
 3. PDF.PrintRenderer

The [first two renderers](/manuals/hosting/mom/rendering-in-windows.html) depend on the Windows operating system as they direct their output to an Windows printer device, the printer can be a 'physical' printer or the _Microsoft Print to PDF_ &nbsp;'printer'. Both of them are also dependent on the .NET Framework.
 
The [third renderer](/manuals/hosting/mom/rendering-in-linux.html), `PDF.PrintRenderer`, creates a PDF document and is independent of the Windows OS. `PDF.PrintRenderer` is a .NET (Core) executable.

## Renderer Command Line Options

A Manuscript Renderer can be called automatically when you close a Printer File but it is also possible to invoke the Renderer from the command line.

These are the parameters available for all versions of the Renderers and their function:

| Parameter | Function
| --------- | --------
| **`/m:"file"`** | Manuscript Path (**required**).
| **`/d`** | Delete manuscript file after rendering is complete.
| **`/q`** | Quiet printing. This hides the print preview window and prints directly.
| **`/r:"page range"`** | Specify page numbers and/or page ranges separated by commas (i.e. 1,3,5-12, *last).
| **`/h`** or **`/?`** | Displays help on parameter usage.

The above parameters can be specified in any order.

### Manuscript Parameter
**`/m:"file"`** — `file` is a path to the manuscript to be rendered. It can be relative to the Renderer.exe's location, and **is always required**.

The "_file_" specified can contain the relative or full path. If you are executing the renderer from the same directory as the manuscript, only the manuscript file name is necessary. For instance. **`"myManuscript.apm"`** as a relative path versus **`"C:/myReports/myManuscript.apm"`** as a full path.

### Delete Parameter
If **`/d`** is not specified, the manuscript file will **not** be deleted after rendering is complete.

### Quiet Parameter
If **`/q`** is not specified, the print preview window will display to allow for the report to be previewed.

### Range Parameter
If the **`/r`** parameter is not specified, **all** pages will be printed or previewed. 

To select single pages, separate each page number with a comma. **`/r:"1,3"`** will print pages 1 and 3. 

To specify a range of pages, enter the first and last page numbers separated with a dash. **`/r:"1-3"`** will print pages 1, 2, and 3.  

The **`*last`** keyword refers to the last page of the document. In addition, you can specify arithmetic operations on **`*last`** in order to print pages **relative** to the last page. For instance **`/r:"*last-2`** " will print the second to the last page, while **`/r:"*last-4 - *last"`** prints the last 5 pages.

A combinations of single page and a range of pages can be specified. **`/r:"1-3, 5,9, *last"`** will print pages 1, 2, 3, 5, 9, and the last page.


## Examples

These example are using the Windows renderer `Renderer.exe` but the same options can be used with the other renderers.

**Print preview the entire report and do not delete Manuscript file when finished (all defaults used).**

`Renderer.exe "C:/myReports/myManuscript.apm"`

**Direct print complete report and delete Manuscript when finished (no preview).**

`Renderer.exe /m:"C:/myReports/myManuscript.apm" /d /q`

`Renderer.exe /q /m:"C:/myOutQ/myManuscript.apm" /d `

**Direct print last page and delete Manuscript when finished (no preview).**

`Renderer.exe /m:"C:/myReports/myManuscript.apm" /d /q /r:"*last"`

**Print preview the first three pages and last three pages, do not delete Manuscript when finished.**

`Renderer.exe /m:"C:/myReports/myManuscript.apm" /r:"1 - 3, *last-2 - *last"`




