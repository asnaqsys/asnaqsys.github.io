---
title: "EscapeFX Edit Record Function"
description: "EscapeFX Edit Record Function"
mermaid: true
---

## EditRecordFunction

The EditRecordFunction](/reference/escapefx/edit-record-function.html) class is an abstract subclass of [SingleRecordProgram](single-record-program.html), tailored for editable single-record applications. It supports adding or changing records, with built-in mode switching and validation. Its primary responsibilities include:

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


## Workflow

<pre class="mermaid">
flowchart TD
    A["EditRecord()"] --> B["ProgramMainLoop()"]
    B --> C["InitProgram()"]
    C --> D["CheckParms()"]
    D --> E["Loop while RepeatDisplay == 'N'"]
    E --> F["DisplayKeyScreen()"]
    F --> G{"EncourageBypass?"}
    G -->|Yes| H["BypassFirstScreen = 'Y'"]
    G -->|No| J
    H --> J["InitKeyScreenFields()"]
    J --> K["IsTransaction = 'Y'"]
    K --> L{"IsTransaction == 'Y' or 'K'?"}
    L -->|Yes| M["IsTransaction = 'Y'"]
    M --> N["ScreenKind = 1"]
    N --> O{"IsTransaction == 'Y'?"}
    O -->|Yes| P["ConvertKeyToExternal()"]
    P --> Q{"BypassFirstScreen == 'Y' and (IsAnyKeyFieldBlank() or RefreshScreenRequested)?"}
    Q -->|Yes| R["BypassFirstScreen = 'N'"]
    Q -->|No| T
    R --> T{"BypassFirstScreen == 'N'?"}
    T -->|Yes| U["ShowKeyScreen()"]
    T -->|No| W
    U --> W["BypassFirstScreen = 'N'"]
    W --> X{"CancelRequested?"}
    X -->|Yes| Y["CancelProgram()"]
    X -->|No| Z{"inF09ChangeMode?"}
    Z -->|Yes| AA["ToggleAddChangeMode()"]
    Z -->|No| BB{"RefreshScreenRequested?"}
    BB -->|Yes| CC["ProcessHome()"]
    BB -->|No| DD{"in26Clear?"}
    DD -->|Yes| EE["RepositionWindow()"]
    DD -->|No| FF["ProcessKeyScreen()"]
    AA --> GG{"IsTransaction == 'R'?"}
    CC --> GG
    EE --> GG
    FF --> GG
    GG -->|Yes| HH["IsTransaction = 'Y'"]
    HH --> II["ProcessKeyScreen()"]
    II --> GG
    GG -->|No| O
    O -->|No| L
    L -->|No| E
    E --> KK["CancelProgram()"]
    Y --> LL["End"]

   subgraph subA [" "]
      A
      VirtualTag["Method is Virtual"]
      AbstractTag["Method is Abstract"]
      class VirtualTag virtual;
      class AbstractTag abstract;
   end

   classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
   classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
   classDef colorKey fill:transparent,stroke-width:0;
   class subA colorKey

   class A,AA,CC virtual;
   class J,FF abstract;

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