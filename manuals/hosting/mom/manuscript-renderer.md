---
title: "Manuscript Open.Renderer and Open.PrintControls"
description: "Explore how to use the Manuscript Renderer for outputing to a printer, including the command line options."
---

The Open.Renderer (Renderer for short) and Open.PrintControls can be used to print a Manuscript file to any printer installed on a **Windows computer**, including the 'Microsoft Print To PDF' printer.

You can read the [Concepts behind printing here](/concepts/printing/printing-introduction.html).

Open.Render is the Open Source release of part of the printing facilities employed by DataGate, these facilities include two components:
 + Renderer
 + PrintControls

> These Components target the .NET Framework.

To distiguish these components from those ship with the standard ASNA products the names have been prefixed with 'Open.'.


## Renderer Command Line Options

A Manuscript Renderer can be called automatically when you close a Printer File.  It is also possible to invoke the Renderer from the command line.

Parameters available for Renderer.exe and their function:

| Parameter | Function
| --------- | --------
| **`/m:"file"`** | Manuscript Path (**required**).
| **`/d`** | Delete manuscript file after rendering is complete.
| **`/q`** | Quiet printing. This hides the print preview window and prints directly.
| **`/r:"page range"`** | Specify page numbers and/or page ranges separated by commas (i.e. 1,3,5-12, \*last).
| **`/h`** or **`/?`** | Displays help on parameter usage.

### General Rules

The above parameters can be specified in any order.

*   `**"file"**` is a path to the manuscript to be rendered. It can be relative to the Renderer.exe's location, and **is always required**.

    The "_file_" specified can contain the relative or full path. If you are executing the renderer from the same directory as the manuscript, only the manuscript file name is necessary. For instance. `**"myManuscript.apm"**` as a relative path versus `**"C:\\myReports\\myManuscript.apm"**` as a full path.

*   If `**/d**` is not specified, the manuscript file will **not** be deleted after rendering is complete.

*   If `**/q**` is not specified, the print preview window will display to allow for the report to be previewed.

*   If `**/r:"page range"**` is not specified, **all** pages will be printed or previewed. 

    To select single pages, separate each page number with a comma. `**/r:"1,3"**` will print pages 1 and 3. 
    
    To specify a range of pages, enter the first and last page numbers separated with a dash. `**/r:"1-3"**` will print pages 1, 2, and 3.  
    
    The `**\*last**` keyword refers to the last page of the document. In addition, you can specify arithmetic operations on `**\*last**` in order to print pages **relative** to the last page. For instance `**/r:"\*last-2**` " will print the second to the last page, while `**/r:"\*last-4 - \*last**`" prints the last 5 pages.
    
    A combinations of single page and a range of pages can be specified. `**/r:"1-3, 5,9, \*last"**` will print pages 1, 2, 3, 5, 9, and the last page.
    

### Examples

**Print preview the entire report and do not delete Manuscript file when finished (all defaults used).**

`Renderer.exe "C:myReports\\myManuscript.apm"`

**Direct print complete report and delete Manuscript when finished (no preview).**

`Renderer.exe /m:"C:\\myReports\\myManuscript.apm" /d /q`

`Renderer.exe /q /m:"C:\\myOutQ\\myManuscript.apm" /d `

**Direct print last page and delete Manuscript when finished (no preview).**

`Renderer.exe /m:"C:\\myReports\\myManuscript.apm" /d /q /r:"\*last"`

**Print preview the first three pages and last three pages, do not delete Manuscript when finished.**

`Renderer.exe /m:"C:\\myReports\\myManuscript.apm" /r:"1 - 3, \*last-2 - \*last"`




