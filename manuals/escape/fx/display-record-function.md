---
title: "EscapeFX Display Record Function"
description: "EscapeFX Display Record Function"
---

## DisplayRecordFunction

Key Responsibilities of DisplayRecordFunction

The _DisplayRecordFunction_ class is an abstract subclass of _SingleRecordProgram_, designed for read-only or display-oriented single-record applications. It provides a framework for presenting record data to users without allowing modifications, emphasizing data retrieval and visualization. Its key responsibilities include:

1. **Driving the Display Workflow**:
   - The **DisplayRecord()** method invokes **ProgramMainLoop()** to initialize and manage the display cycle, ensuring the program runs until completion or cancellation.

2. **Key Screen Management**:
   - Overrides **DisplayKeyScreen()** to handle key field input and display, bypassing the first screen if possible (**BypassFirstScreen = "Y"**) and processing user responses like cancel, refresh, or repositioning.
   - Initializes key screen fields and manages transaction states for seamless navigation.

3. **User Interaction Handling**:
   - Processes standard commands (e.g., cancel via **CancelProgram()**, refresh via **ProcessHome()**, clear via **RepositionWindow()**) and delegates specific key screen processing to the abstract **ProcessKeyScreen()** method.
   - Supports reprocessing loops for repeated input validation.

4. **Data Conversion and Display Conditioning**:
   - Relies on inherited methods for converting key fields to external formats and setting display attributes, ensuring data is presented correctly without modification capabilities.

5. **Integration with Framework Infrastructure**:
   - Inherits multi-screen support and validation from _SingleRecordProgram_, but focuses on display-only operations (e.g., no add/change modes).
   - Provides hooks for subclasses to implement key screen processing and field initialization, promoting reusability for display-centric applications.

In summary, _DisplayRecordFunction_ specializes in read-only record presentation, abstracting display logic while requiring subclasses to handle user inputs and data setup, making it ideal for inquiry or reporting screens.


## Flowchart

```mermaid

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

```

## Class Diagram

```mermaid
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram

    class DisplayRecordFunction {
        +DisplayRecord() virtual
        +DisplayKeyScreen() override
    }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SingleRecordProgram
   SingleRecordProgram <|-- DisplayRecordFunction
    
```