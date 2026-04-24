---
title: "EscapeFX Display Transaction Function"
description: "EscapeFX Display Transaction Function"
---

## DisplayTransactionFunction

The <u>DisplayTransactionFunction</u> class is an abstract subclass of <u>SubfileProgram</u>, designed for read-only display of transactional data in subfiles. It focuses on presenting data without allowing modifications, supporting screen initialization and navigation. Its primary responsibilities include:

1. **Transaction Display Workflow**:
   - The **DisplayTransaction()** method initializes the program and conducts a loop for displaying screens, bypassing the first screen on initial cycles (<u>FirstCycle</u>) and handling user responses like cancel or refresh.

2. **Screen and Subfile Initialization**:
   - Requires subclasses to implement **InitScreen()** for setting up screen fields and subfile data.
   - Overrides **ClearSubfile()** to reset subfile records and counters for clean displays.

3. **Data Conversion and Display**:
   - Provides **ConvertControlToExternal()** (virtual) for converting control fields to external formats and overrides **ConvertMajorFieldsToExternalForm()** to integrate with subfile rendering.

4. **User Interaction Handling**:
   - Processes commands such as cancel (via **CancelProgram()**), refresh (via **ProcessHomeKey()**), and delegates subfile processing to inherited methods.
   - Manages transaction states and cursor clearing for seamless navigation.

5. **Integration with Framework Infrastructure**:
   - Inherits subfile management from <u>SubfileProgram</u>, focusing on display-only operations without edit capabilities.
   - Allows subclasses to customize initialization and conversion, enabling flexible read-only transactional views.

In summary, <u>DisplayTransactionFunction</u> specializes in presenting transactional subfile data, abstracting display logic while requiring subclasses to handle setup and data conversion.


## Flowchart

```mermaid

flowchart TD
    A["DisplayTransaction()"] --> B["InitProgram()"]
    B --> C["FirstCycle = 'Y'"]
    C --> D["Loop while true"]
    D --> E["InitScreen()"]
    E --> F{"IsTransaction == 'Y'?"}
    F -->|Yes| G["ConvertControlToExternal()"]
    G --> H{"FirstCycle != 'Y'?"}
    H -->|Yes| I["ShowScreen()"]
    H -->|No| K
    I --> K["FirstCycle = 'N'"]
    K --> L{"CancelRequested?"}
    L -->|Yes| M["CancelProgram()"]
    L -->|No| N{"RefreshScreenRequested?"}
    N -->|Yes| O["ProcessHomeKey()"]
    N -->|No| P["ProcessSubfile()"]
    O --> F
    P --> F
    F -->|No| Q{"SetCursor == 'Y'?"}
    Q -->|Yes| R["ClearCursor()"]
    Q -->|No| S{"IsTransaction == 'N'?"}
    R --> S
    S -->|Yes| T["FirstCycle = 'Y'"]
    T --> U["RefreshScreenRequested = false"]
    U --> D
    S -->|No| D
    M --> V["End"]

    classDef virtual fill:#ff9800,stroke:#e65100,stroke-width:2px;
    classDef abstract fill:#2196f3,stroke:#0d47a1,stroke-width:2px;
    class A,G,O virtual;
    class E abstract;
```


## Class Diagram

```mermaid
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram

   class DisplayTransactionFunction {
      +FirstCycle
      +InitScreen() abstract
      +ConvertControlToExternal() virtual
      +ProcessHomeKey() virtual
      +ConvertMajorFieldsToExternalForm() override
      +ClearSubfile() override
      +DisplayTransaction() virtual
   }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SubfileProgram
   SubfileProgram <|-- DisplayTransactionFunction
```

