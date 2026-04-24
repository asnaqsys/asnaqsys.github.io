---
title: "EscapeFX Display File Function"
description: "EscapeFX Display File Function"
---

## DisplayFileFunction

The <u>DisplayFileFunction</u> class is an abstract subclass of <u>SubfileProgram</u>, focused on displaying file records in subfiles without editing. It supports loading, viewing, and basic processing. Its primary responsibilities include:

1. **File Display Workflow**:
   - The **DisplayFile()** method initializes the program and loops through subfile initialization, display, and user response handling.

2. **Subfile Initialization and Loading**:
   - Requires subclasses to implement **InitSubfile()** for setup and **LoadSubfile()** for record loading.
   - Provides **EstablishSubfileLimits()** for computing subfile limits during reading.

3. **Screen Display and Processing**:
   - Overrides **ShowScreen()** to reset invite and error indicators.
   - Processes commands like cancel, refresh, page-down, and delegates input to **ProcessScreen()**.

4. **Subfile Record Processing**:
   - Overrides **ProcessSubfile()** to read and process changed records, updating displays.
   - Offers virtual methods like **ProcessSubfileRecord()** and **UpdateSubfileRecordDB()** for optional customization.

5. **Data Conversion and Updates**:
   - Provides **ConvertControlToExternal()** (virtual) and overrides **ConvertMajorFieldsToExternalForm()**.
   - Includes **UpdateSubfileDB()** for processing modified records if displayed.

6. **Integration with Framework Infrastructure**:
   - Inherits subfile features from <u>SubfileProgram</u>, focusing on read-only file displays.
   - Overrides **CancelProgram()** for simple exit, allowing subclasses to customize loading and processing.

In summary, <u>DisplayFileFunction</u> enables read-only subfile displays of file data, abstracting display logic while supporting extensible loading and processing.


## Flowchart

```mermaid

flowchart TD
    A["DisplayFile()"] --> B["InitProgram()"]
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
   class C,L,M abstract;
   class PR,UR virtual;

```
   
## Class Diagram

```mermaid
---
  config:
    class:
      hideEmptyMembersBox: true
---

classDiagram
   class DisplayFileFunction {
      +InitSubfile() abstract
      +LoadSubfile() abstract
      +ProcessScreen() abstract
      +ProcessSubfileRecord() virtual
      +UpdateSubfileRecordDB() virtual
      +ConvertControlToExternal() virtual
      +DisplayFile() virtual
      +ShowScreen() override
      +ProcessSubfile() override
      +UpdateSubfileDB() virtual
      +EstablishSubfileLimits() virtual
      +ConvertMajorFieldsToExternalForm() override
      +CancelProgram() override
   }

   EscapeProgram <|-- InteractiveProgram 
   InteractiveProgram <|-- SubfileProgram
   SubfileProgram <|-- DisplayFileFunction

```