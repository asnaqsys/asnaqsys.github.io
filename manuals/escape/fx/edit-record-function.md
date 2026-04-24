---
title: "EscapeFX Edit Record Function"
description: "EscapeFX Edit Record Function"
mermaid: true
---

## EditRecordFunction

The _EditRecordFunction_ class is an abstract subclass of _SingleRecordProgram_, tailored for editable single-record applications. It supports adding or changing records, with built-in mode switching and validation. Its primary responsibilities include:

1. **Driving the Edit Workflow**:
   - The **EditRecord()** method calls **ProgramMainLoop()** to manage the edit cycle, initializing and looping through key screen interactions until the program ends.

2. **Key Screen and Mode Management**:
   - Overrides **DisplayKeyScreen()** to handle key field input, mode toggling (e.g., between "ADD" and "CHG" via **ToggleAddChangeMode()**), and user responses like cancel or refresh.
   - Sets _EncourageBypass_ to potentially skip initial displays and manages transaction states for edit operations.

3. **User Interaction and Mode Switching**:
   - Processes commands such as cancel, mode changes (_inF09ChangeMode_), refresh, and repositioning, delegating detailed processing to **ProcessKeyScreen()**.
   - Automatically determines initial mode based on file record count (ADD if empty, CHG otherwise) and updates display attributes accordingly (e.g., **SetDisplayKeyAttributes()** sets _in89AddMode_).

4. **Data Conversion and Validation**:
   - Supports key field conversion and screen initialization, with overrides for mode-specific conditioning.
   - Integrates with inherited validation and confirmation mechanisms for editing workflows.

5. **Integration with Framework Infrastructure**:
   - Builds on _SingleRecordProgram_'s multi-screen and validation features, adding edit-specific logic like mode persistence and attribute setting.
   - Requires subclasses to implement abstract methods for custom key screen handling, enabling flexible edit applications (e.g., forms for data entry or updates).

In summary, _EditRecordFunction_ focuses on mutable record interactions, providing mode management and edit controls while delegating specifics to subclasses, suitable for data entry or modification screens.


## Flowchart

<pre class="mermaid">
flowchart TD
    A["DisplayRecord()"] --> B["ProgramMainLoop()"]
    B --> C["InitProgram()"]
    C --> D["CheckParms()"]
    D --> E["Loop while RepeatDisplay == 'N'"]
    E --> F["DisplayKeyScreen()"]
    F --> G["InitKeyScreenFields()"]
    G --> H["BypassFirstScreen = 'Y'"]
    H --> I["IsTransaction = 'Y'"]
    I --> J{"IsTransaction == 'Y' or 'K'?"}
    J -->|Yes| K["IsTransaction = 'Y'"]
    K --> L["ScreenKind = 1"]
    L --> M{"IsTransaction == 'Y'?"}
    M -->|Yes| N["ConvertKeyToExternal()"]
    N --> O{"BypassFirstScreen == 'Y' and (IsAnyKeyFieldBlank() or RefreshScreenRequested)?"}
    O -->|Yes| P["BypassFirstScreen = 'N'"]
    O -->|No| R
    P --> R{"BypassFirstScreen != 'Y'?"}
    R -->|Yes| S["ShowKeyScreen()"]
    R -->|No| U
    S --> U["BypassFirstScreen = 'N'"]
    U --> V{"CancelRequested?"}
    V -->|Yes| W["CancelProgram()"]
    V -->|No| X{"RefreshScreenRequested?"}
    X -->|Yes| Y["ProcessHome()"]
    X -->|No| Z{"in26Clear?"}
    Z -->|Yes| AA["RepositionWindow()"]
    Z -->|No| BB["ProcessKeyScreen()"]
    Y --> CC{"IsTransaction == 'R'?"}
    AA --> CC
    BB --> CC
    CC -->|Yes| DD["IsTransaction = 'Y'"]
    DD --> EE["ProcessKeyScreen()"]
    EE --> CC
    CC -->|No| M
    M -->|No| J
    J -->|No| E
    E --> GG["CancelProgram()"]
    W --> HH["End"]

    classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
    classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
    class A,N,Y virtual;
    class G,BB abstract;

</pre>

## Class Diagram

<pre class="mermaid">
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram

    class EditRecordFunction {
        +EditRecord() virtual
        +DisplayKeyScreen() override
        +ToggleAddChangeMode() virtual
        +SetDisplayKeyAttributes() override
    }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SingleRecordProgram
   SingleRecordProgram <|-- EditRecordFunction
    
   link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
   link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
   link SingleRecordProgram          "single-record-program.html"          "class SingleRecordProgram"

</pre>