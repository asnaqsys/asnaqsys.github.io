---
title: "EscapeFX Edit Transaction Function"
description: "EscapeFX Edit Transaction Function"
mermaid: true
---

## EditTransactionFunction

The <u>EditTransactionFunction</u> class is an abstract subclass of <u>SubfileProgram</u>, tailored for editable transactional subfiles. It supports adding or changing records, with mode switching and subfile management. Its primary responsibilities include:

1. **Transaction Editing Workflow**:
   - The **EditTransaction()** method initializes the program and loops through screen conversations, handling mode-based bypassing and processing user inputs like mode toggles or page navigation.

2. **Mode Management and Initialization**:
   - Automatically sets <u>ProgramMode</u> to "ADD" or "CHG" based on file record count via overridden **InitMainFileInfo()**.
   - Provides **ToggleAddChangeMode()** for switching modes and resetting transactions.

3. **Screen and Subfile Handling**:
   - Requires **InitScreen()** for screen setup and offers **InitSubfile()** (virtual) for filling subfile pages with blank records.
   - Overrides **ClearSubfile()** to reset subfile state and supports page-down loading.

4. **Data Conversion and Processing**:
   - Includes **ConvertControlToExternal()** and **ConvertControlToInternal()** (virtual) for bidirectional field conversion.
   - Overrides **ConvertMajorFieldsToExternalForm()** to handle control field display.

5. **User Interaction and Validation**:
   - Processes commands like cancel, mode changes, refresh, and delegates subfile processing to **ProcessSubfile()**.
   - Manages transaction states, confirmation, and cursor handling.

6. **Integration with Framework Infrastructure**:
   - Builds on <u>SubfileProgram</u>'s subfile features, adding edit-specific logic like rollback mode and indicator management.
   - Enables subclasses to implement custom initialization and conversion for transactional editing.

In summary, <u>EditTransactionFunction</u> focuses on editable transactional subfiles, providing mode switching and processing hooks while inheriting core subfile functionality.


## Flowchart

<pre class="mermaid">

flowchart TD
    A["EditTransaction()"] --> B["InitProgram()"]
    B --> C["Loop while true"]
    C --> D["InitScreen()"]
    D --> E["Set BypassFirstScreen"]
    E --> F{"IsTransaction == 'Y'?"}
    F -->|Yes| G["ConvertControlToExternal()"]
    G --> H{"BypassFirstScreen != 'Y'?"}
    H -->|Yes| I["ShowScreen()"]
    H -->|No| J["clearCommandKeyIndicators()"]
    I --> K["BypassFirstScreen = 'N'"]
    J --> K
    K --> L{"CancelRequested?"}
    L -->|Yes| M["CancelProgram()"]
    L -->|No| N{"inF09ChangeMode?"}
    N -->|Yes| O["ToggleAddChangeMode()"]
    N -->|No| P{"RefreshScreenRequested?"}
    P -->|Yes| Q["ProcessHomeKey()"]
    P -->|No| S
    O --> S{"IsTransaction == 'Y'?"}
    Q --> S
    S -->|Yes| T["ConvertControlToInternal()"]
    T --> U{"in27PageDown?"}
    U -->|Yes| V["InitSubfile()"]
    U -->|No| W["ProcessSubfile()"]
    V --> F
    W --> F
    S -->|No| X{"SetCursor == 'Y'?"}
    X -->|Yes| Y["ClearCursor()"]
    X -->|No| C
    Y --> C
    M --> Z["End"]

    classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
    classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
    class A,G,Q,T,V virtual;
    class D abstract;

</pre>

## Class Diagram

<pre class="mermaid">
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram

    class EditTransactionFunction {
        +RollBackMode
        +InitScreen() abstract
        +InitSubfile() virtual
        +ConvertControlToExternal() virtual
        +ConvertControlToInternal() virtual
        +ProcessHomeKey() virtual
        +ConvertMajorFieldsToExternalForm() override
        +ClearSubfile() override
        +EditTransaction() virtual
        +ToggleAddChangeMode()
        +InitMainFileInfo() override
    }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SubfileProgram
   SubfileProgram <|-- EditTransactionFunction

   link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
   link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
   link SubfileProgram               "subfile-program.html"                "class SubfileProgram"

</pre>

