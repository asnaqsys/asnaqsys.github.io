---
title: "EscapeFX Subfile Program"
description: "EscapeFX Subfile Program"
mermaid: true
---

## SubfileProgram

The <u>SubfileProgram</u> class is an abstract base class in the ASNA.QSys.EscapeFX framework, extending <u>InteractiveProgram</u> to provide infrastructure for managing subfile-based user interfaces (e.g., scrollable lists or tables of records). It handles subfile initialization, loading, prompting, and processing, supporting multi-page displays and record navigation. Its primary responsibilities include:

1. **Subfile Management and Initialization**:
   - Initializes subfile-related fields (e.g., <u>SubfileRRN</u>, <u>MaxSubfileRRN</u>, scan limits) and overrides **InitProgram()** to set up subfile parameters like pages and records per page.
   - Provides methods like **establishSubfileLimits()** to compute required lines and pages for subfile loading.

2. **Screen Display and Subfile Rendering**:
   - Overrides **ShowScreen()** to handle subfile control formats, maintain subfile positions, and process prompts within subfile rows.
   - Includes **clearSubfileRecord()** and **ClearSubfile()** for resetting subfile contents and record counts.

3. **Prompting and Cursor Handling in Subfiles**:
   - Overrides **ProcessPrompt()** to resolve prompt rows within subfiles, read changed records, and update subfile data.
   - Offers **SetCursorInSubfile()** for positioning cursors in subfile fields and **SetPromptRows()** for defining promptable row ranges.

4. **Record Processing and Validation**:
   - Provides virtual methods like **ProcessSubfile()** for processing modified subfile records and **SaveHighestSFLRecord()** for tracking load progress.
   - Includes utilities like **CheckDBFRecordsFound()** for error handling when no records are available and **CheckScanLimit()** for limiting record scans.

5. **Data Conversion and Display Attributes**:
   - Requires subclasses to implement **ConvertMajorFieldsToExternalForm()** for converting control fields to display formats.
   - Supports virtual methods for setting display attributes (**SetDisplayAttributes()**, **SetDisplayControlAttributes()**) and resetting screen fields.

6. **Integration with Framework Infrastructure**:
   - Inherits interactive features from <u>InteractiveProgram</u>, adding subfile-specific indicators (e.g., <u>in80ClearSubfile</u>, <u>in81DisplaySubfile</u>) and fields for RRN tracking and paging.
   - Enables extensibility through virtual methods, allowing subclasses to customize subfile behavior without altering core logic.

In summary, <u>SubfileProgram</u> abstracts subfile operations, providing reusable components for loading, displaying, and interacting with record lists, while delegating specifics to subclasses.


## No Flowchart

The Subfile Program class does not include a workflow implementation, that is left to its derived classes to provide.


## Class Diagrams

<pre class="mermaid">
---
  config:
    class:
      hideEmptyMembersBox: true
---
classDiagram
    class SubfileProgram {
        +ProcessSubfile() virtual
        +CheckDBFRecordsFound()
        +ProcessSubfileNamePrompt()
        +SaveHighestSFLRecord()
        +establishSubfileLimits() virtual
        +CheckScanLimit()
        +RequestReloadSubfile()
        +SetCursorInSubfile()
        +InitProgram() override
        +clearSubfileRecord()
        +ClearSubfile() virtual
        +SetDisplayAttributes() virtual
        +SetDisplayControlAttributes() virtual
        +ResetScreenFields() virtual
        +ShowScreen() virtual
        +ResolvePromptRow() virtual
        +ProcessPrompt() override
        +SetPromptRows()
        +ConvertMajorFieldsToExternalForm() abstract
    }

    EscapeProgram <|-- InteractiveProgram 
    InteractiveProgram <|-- SubfileProgram
    SubfileProgram <|-- DisplayTransactionFunction
    SubfileProgram <|-- EditTransactionFunction
    SubfileProgram <|-- SelectRecordFunction
    SubfileProgram <|-- DisplayFileFunction
    SubfileProgram <|-- EditFileFunction

   link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
   link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
   link DisplayFileFunction          "display-file-function.html"          "class DisplayFileFunction"
   link DisplayTransactionFunction   "display-transaction-function.html"   "class DisplayTransactionFunction"
   link EditFileFunction             "edit-file-function.html"             "class EditFileFunction"
   link EditTransactionFunction      "edit-transaction-function.html"      "class EditTransactionFunction"
   link SelectRecordFunction         "select-record-function.html"         "class SelectRecordFunction"


</pre>