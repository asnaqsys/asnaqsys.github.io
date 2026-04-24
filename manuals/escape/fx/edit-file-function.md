---
title: "EscapeFX Edit File Function"
description: "EscapeFX Edit File Function"
mermaid: true
---

## EditFileFunction

The <u>EditFileFunction</u> class is an abstract subclass of <u>SubfileProgram</u>, designed for editing file records in subfiles. It supports adding, changing, and updating records with mode switching. Its primary responsibilities include:

1. **File Editing Workflow**:
   - The **EditFile()** method initializes the program and loops through subfile loading, display, and user input processing.

2. **Subfile Initialization and Loading**:
   - Offers virtual **InitSubfile()** and **LoadSubfile()** for setup and population.
   - Provides **EstablishSubfileLimits()** for computing limits during writing.

3. **Screen Display and Processing**:
   - Processes commands like cancel, refresh, page-down, and delegates to **ProcessScreen()**.
   - Overrides display attributes to handle add/change modes and field protection.

4. **Subfile Record Processing and Updates**:
   - Overrides **ProcessSubfile()** to process changed records and update displays.
   - Requires **ProcessSubfileRecord()** and **UpdateSubfileRecordDB()** for custom logic.
   - Provides **UpdateSubfileDB()** for committing changes to the database.

5. **Mode Management and Data Conversion**:
   - Includes **ToggleAddChangeMode()** for switching modes and requesting reloads.
   - Overrides **ConvertMajorFieldsToExternalForm()** and offers **ConvertControlToExternal()**.

6. **Prompting and Cursor Handling**:
   - Overrides **ResolvePromptRow()** to handle subfile prompting and chaining.

7. **Integration with Framework Infrastructure**:
   - Builds on <u>SubfileProgram</u> for subfile operations, adding edit capabilities like mode indicators and updates.
   - Enables subclasses to implement record processing and updates for flexible file editing.

In summary, <u>EditFileFunction</u> supports editable subfile interfaces for file records, providing mode management and update hooks while inhering core subfile functionality.


## Flowchart

<pre class="mermaid">

flowchart TD
    A["EditFile()"] --> B["InitProgram()"]
    B --> C["InitSubfile()"]
    C --> D["ReloadSubfile = 'N'"]
    D --> E{"ReloadSubfile == 'N'?"}
    E -->|Yes| F["ShowScreen()"]
    F --> G{"CancelRequested?"}
    G -->|Yes| H["CancelProgram()"]
    G -->|No| I{"RefreshScreenRequested?"}
    I -->|Yes| J["RequestReloadSubfile()"]
    I -->|No| K{"in27PageDown?"}
    K -->|Yes| L["LoadSubfile()"]
    K -->|No| M["ProcessScreen()"]
    M --> PR["ProcessSubfileRecord()"]
    M --> UR["UpdateSubfileRecordDB()"]
    H --> N["End"]
    J --> E
    L --> E
    M --> E
    E -->|No| O["Loop back"]
    O --> C

    classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
    classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
    class C,L,M virtual;
    class PR,UR abstract;

</pre>

## Class Diagram

<pre class="mermaid">
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram
    class EditFileFunction {
        +InitSubfile() virtual
        +LoadSubfile() virtual
        +ProcessScreen() virtual
        +ProcessSubfileRecord() abstract
        +UpdateSubfileRecordDB() abstract
        +ConvertControlToExternal() virtual
        +EditFile() virtual
        +ProcessSubfile() override
        +UpdateSubfileDB() virtual
        +EstablishSubfileLimits() virtual
        +SetDisplayAttributes() override
        +SetDisplayControlAttributes() override
        +ToggleAddChangeMode()
        +ConvertMajorFieldsToExternalForm() override
        +ResolvePromptRow() override
    }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SubfileProgram
   SubfileProgram <|-- EditFileFunction

   link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
   link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
   link SubfileProgram               "subfile-program.html"                "class SubfileProgram"

</pre>