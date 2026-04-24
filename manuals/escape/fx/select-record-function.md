---
title: "EscapeFX Select Record Function"
description: "EscapeFX Select Record Function"
mermaid: true
---

## SelectRecordFunction

The <u>SelectRecordFunction</u> class is an abstract subclass of <u>SubfileProgram</u>, designed for selecting records from subfiles. It supports loading, displaying, and processing selections without editing. Its primary responsibilities include:

1. **Record Selection Workflow**:
   - The **SelectRecord()** method initializes the program and loops through subfile loading, display, and user response processing until a selection or cancel occurs.

2. **Subfile Initialization and Loading**:
   - Requires subclasses to implement **InitSubfile()** for subfile setup and **LoadSubfile()** for populating records.
   - Provides **EstablishSubfileLimits()** to compute subfile limits for reading.

3. **Screen Display and Processing**:
   - Overrides **ShowScreen()** to reset invite and error indicators after display.
   - Handles user commands like cancel, refresh, page-down (via **LoadSubfile()**), and delegates screen input to **ProcessScreen()**.

4. **Subfile Record Processing**:
   - Overrides **ProcessSubfile()** to read and process changed subfile records, updating displays and handling errors.
   - Requires **ProcessSubfileRecord()** for custom record processing logic.

5. **Data Conversion and Cancellation**:
   - Offers **ConvertControlToExternal()** (virtual) and overrides **ConvertMajorFieldsToExternalForm()** for field conversion.
   - Overrides **CancelProgram()** to send a "no value selected" message and exit.

6. **Integration with Framework Infrastructure**:
   - Inherits subfile management from <u>SubfileProgram</u>, emphasizing selection over editing.
   - Allows subclasses to define loading and processing, enabling flexible record selection interfaces.

In summary, <u>SelectRecordFunction</u> specializes in subfile-based record selection, abstracting workflow and processing while requiring subclasses to handle data loading and user input.


## Flowchart

<pre class="mermaid">

flowchart TD
    A["SelectRecord()"] --> B["InitProgram()"]
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
    H --> N["End"]
    J --> E
    L --> E
    M --> E
    E -->|No| O["Loop back"]
    O --> C

    classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
    classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
    class A virtual;
    class C,L,M,PR abstract;

</pre>

## Class Diagram

<pre class="mermaid">
---
  config:
    class:
      hideEmptyMembersBox: true
---
classDiagram
   class SelectRecordFunction {
      +InitSubfile() abstract
      +LoadSubfile() abstract
      +ProcessScreen() abstract
      +ProcessSubfileRecord() abstract
      +ConvertControlToExternal() virtual
      +ConvertMajorFieldsToExternalForm() override
      +SelectRecord() virtual
      +ShowScreen() override
      +ProcessSubfile() override
      +EstablishSubfileLimits() virtual
      +CancelProgram() override
   }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SubfileProgram
   SubfileProgram <|-- SelectRecordFunction

   link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
   link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
   link SubfileProgram               "subfile-program.html"                "class SubfileProgram"

</pre>