---
title: "EscapeFX Single Record Function"
description: "EscapeFX Single Record Function"
mermaid: true
---

## SingleRecordProgram

The *SingleRecordProgram* class is an abstract base class in the ASNA.QSys.EscapeFX framework, extending *InteractiveProgram* to provide a structured foundation for single-record-based user interactions. It manages the overall program flow for applications that handle individual records (e.g., display or edit operations), supporting multi-screen workflows and record validation. Its primary responsibilities include:

1.  **Managing the Main Program Loop**:
    *   The **ProgramMainLoop()** method initializes the program, checks parameters, and repeatedly calls **DisplayKeyScreen()** until *RepeatDisplay* indicates no repetition. This ensures the program can handle multiple iterations for record processing or re-display.

2.  **Screen Display and Multi-Screen Support**:
    *   Provides methods like **ShowKeyScreen()** and **ShowScreen()** for rendering key and detail screens, handling help requests, cursor positioning, and window management.
    *   Supports up to three screen kinds (e.g., for paginated details), with indicator arrays (*Screen1Indicators*, etc.) for conditioning screen elements.
    *   Includes navigation logic for rolling between screens (e.g., **DisplayNextScreen()**, **DisplayPreviousScreen()**) and error handling per screen.

3.  **Record Validation and Processing**:
    *   **ValidateRecord()** orchestrates validation, confirmation prompts, and record processing, deferring to virtual methods like **ValidateDetails()** and **ProcessRecord()** for customization.
    *   Handles transaction states (e.g., "Y" for active, "R" for reprocess) and integrates with confirmation mechanisms.

4.  **Data Conversion and Initialization**:
    *   Offers hooks for converting key fields to external formats (**ConvertKeyToExternal()**) and initializing/resetting screen fields via abstract methods (**InitKeyScreenFields()**, **ResetScreenFields()**).
    *   Manages screen indicators and cursor settings for different panels.

5.  **Integration with Framework Infrastructure**:
    *   Inherits interactive features from *InteractiveProgram*, such as prompting, messaging, and indicator management.
    *   Provides abstract methods (**DisplayKeyScreen()**, **ProcessKeyScreen()**) that subclasses must implement to define specific key screen behavior and input processing.
    *   Supports extensibility through virtual methods, allowing subclasses to customize validation, display attributes, and cursor handling without altering the core loop.

In summary, *SingleRecordProgram* abstracts the complexities of single-record workflows, enabling subclasses to focus on domain-specific logic while ensuring consistent screen handling, validation, and user interaction patterns.


## Flowchart

<pre class="mermaid">

flowchart TD
    A["ProgramMainLoop()"] --> B["InitProgram()"]
    B --> C["CheckParms()"]
    C --> D["Loop while RepeatDisplay == 'N'"]
    D --> E["DisplayKeyScreen()"]
    E --> D
    D --> F["CancelProgram()"]
    F --> G["End"]

    classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
    classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
    class A,C virtual;
    class E abstract;

</pre>

## Class Diagrams
<pre class="mermaid">
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram
    class SingleRecordProgram {
        +ProgramMainLoop() virtual
        +ShowKeyScreen() virtual
        +DisplayScreen() virtual
        +ValidateRecord() virtual
        +SetDisplayAttributes() virtual
        +SetDisplayKeyAttributes() virtual
        +ClearScreenIndicators()
        +ErrorsInScreen()
        +IsAnyKeyFieldBlank() virtual
        +ValidateDetails() virtual
        +ProcessRecord() virtual
        +CheckParms() virtual
        +ConvertKeyToExternal() virtual
        +SetCursor1() virtual
        +SetCursor2() virtual
        +SetCursor3() virtual
        +DisplayKeyScreen() abstract
        +ProcessKeyScreen() abstract
        +ResetScreenFields() abstract
        +InitKeyScreenFields() abstract
    }


    EscapeProgram <|-- InteractiveProgram 
    InteractiveProgram <|-- SingleRecordProgram
    SingleRecordProgram <|-- DisplayRecordFunction
    SingleRecordProgram <|-- EditRecordFunction
    
    link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
    link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
    link DisplayRecordFunction        "display-record-function.html"        "class DisplayRecordFunction"
    link EditRecordFunction           "edit-record-function.html"           "class EditRecordFunction"

</pre>