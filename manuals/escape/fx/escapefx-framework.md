---
title: "ASNA QSys EscapeFX Library"
description: "Introduction to the ASNA.QSys.EscapeFX Framework"
mermaid: true
---

The ASNA.QSys.EscapeFX framework is a comprehensive, object-oriented library designed to simplify the development of business applications in .NET environments, particularly those migrating from legacy systems like IBM i (AS/400). Implemented in the *ASNA.QSys.EscapeFX* namespace, it provides a structured hierarchy of abstract base classes that encapsulate common program patterns, user interactions, data handling, and system integrations. This framework abstracts low-level details such as program initialization, messaging, database operations, and UI management, allowing developers to focus on domain-specific logic while ensuring consistency, reusability, and maintainability.

# Framework Architecture

At its core, the framework follows a hierarchical inheritance model, with *EscapeProgram* as the root abstract class extending *ASNA.QSys.Runtime.JobSupport.Program*. This base class establishes the foundation for all programs, handling essential lifecycle management, error handling, and system utilities. It includes features like program status data structures, indicator management (e.g., for error flags), messaging queues, date/time conversions, string manipulations, and database record locking. Subclasses build upon this by adding specialized capabilities for different application types.

The hierarchy branches into several key categories:

*   **Interactive Programs**: Classes like *InteractiveProgram* extend *EscapeProgram* to support user-facing applications with screen-based interactions. They manage workstation files, prompting mechanisms, cursor positioning, window layouts, and validation for fields like dates and numerics.
*   **Subfile-Based Programs**: *SubfileProgram* further specializes for applications displaying scrollable lists (subfiles) of records. It handles subfile initialization, loading, prompting within subfiles, and multi-page navigation, supporting complex data presentations.
*   **Specific Interaction Patterns**: Concrete subclasses such as *PromptRecordFunction*, *SingleRecordProgram* (with variants like *DisplayTransactionFunction*, *EditTransactionFunction*, *SelectRecordFunction*, *DisplayFileFunction*, and *EditFileFunction*), and *SubfileProgram* derivatives provide tailored workflows. For instance, *PromptRecordFunction* drives prompt-based record interactions, while *SingleRecordProgram* manages single-record displays or edits with support for multiple screens.
*   **Non-Interactive Programs**: *PrintFunction* enables report generation by managing print files, page formatting, and output controls. *ExternalFunction* serves as a lightweight base for generic programs without predefined I/O, allowing custom logic implementation.

Supporting classes like *PrintObject* and *PrintFlag* assist in print operations, while enums and utilities enhance functionality across the framework.

# Key Responsibilities and Benefits

Each class in the hierarchy has well-defined responsibilities:

*   **EscapeProgram**: Provides universal program infrastructure, including initialization (**InitProgram()**), messaging (**SendMessage()**, **SendErrorMessage()**), data validation (e.g., **ValidateExternalDate()**, **ScanField()**), database interactions (e.g., **LockForUpdate()**, **HasRecordChanged()**), and job submission (**SubmitterNewRequest()**). It ensures consistent error handling and system integration.
*   **InteractiveProgram**: Adds UI-focused features like screen display (**ShowScreen()**), prompting (**ProcessPrompt()**), cursor management (**SetCursor0()**, **TestCursor()**), and window positioning (**SetWindowLocation()**). It supports confirmation prompts and name prompting for enhanced user experiences.
*   **SubfileProgram**: Manages subfile-specific operations, including record loading, prompting within subfiles (**ProcessPrompt()**), and navigation (**DisplayNextScreen()**, **DisplayPreviousScreen()**). It integrates with interactive features for complex list-based interfaces.
*   **Specialized Subclasses**: Classes like *DisplayTransactionFunction* handle read-only transactional displays, *EditTransactionFunction* supports editable transactions with mode switching, and *PrintFunction* orchestrates report workflows (**PrintFile()**), including page headers and overflow handling.

The framework promotes separation of concerns by abstracting repetitive tasks, reducing boilerplate code, and enforcing best practices. It facilitates rapid development of maintainable applications, supports legacy system migrations, and integrates seamlessly with ASNA's runtime environment. By leveraging inheritance, developers can override virtual methods (e.g., **InitProgram()**, **ProcessScreen()**) to customize behavior while inheriting robust, tested functionality.

In summary, the ASNA.QSys.EscapeFX framework empowers developers to build scalable, user-centric business applications efficiently. Its modular design ensures that from simple external functions to complex interactive subfile programs, the framework adapts to diverse needs, fostering productivity and reliability in modern .NET ecosystems. For detailed implementation, refer to the class diagrams and API documentation.


## Class Herachy

<pre class="mermaid">

classDiagram
    class DisplayFileFunction
    class DisplayRecordFunction
    class DisplayTransactionFunction
    class EditFileFunction
    class EditRecordFunction
    class EditTransactionFunction
    class EscapeProgram
    class ExternalFunction
    class InteractiveProgram
    class PrintFunction
    class PromptRecordFunction
    class SelectRecordFunction
    class SingleRecordProgram
    class SubfileProgram
    link DisplayFileFunction          "display-file-function.html"          "class DisplayFileFunction"
    link DisplayRecordFunction        "display-record-function.html"        "class DisplayRecordFunction"
    link DisplayTransactionFunction   "display-transaction-function.html"   "class DisplayTransactionFunction"
    link EditFileFunction             "edit-file-function.html"             "class EditFileFunction"
    link EditRecordFunction           "edit-record-function.html"           "class EditRecordFunction"
    link EditTransactionFunction      "edit-transaction-function.html"      "class EditTransactionFunction"
    link EscapeProgram                "escape-program.html"                 "class EscapeProgram"
    link ExternalFunction             "external-function.html"              "class ExternalFunction"
    link InteractiveProgram           "interactive-program.html"            "class InteractiveProgram"
    link PrintFunction                "print-function.html"                 "class PrintFunction"
    link PromptRecordFunction         "prompt-record-function.html"         "class PromptRecordFunction"
    link SelectRecordFunction         "select-record-function.html"         "class SelectRecordFunction"
    link SingleRecordProgram          "single-record-program.html"          "class SingleRecordProgram"
    link SubfileProgram               "subfile-program.html"                "class SubfileProgram"

    EscapeProgram <|-- PrintFunction
    EscapeProgram <|-- ExternalFunction
    EscapeProgram <|-- InteractiveProgram
    InteractiveProgram  <|-- PromptRecordFunction
    InteractiveProgram <|-- SubfileProgram
    SubfileProgram <|-- DisplayTransactionFunction
    SubfileProgram <|-- EditTransactionFunction
    SubfileProgram <|-- SelectRecordFunction
    SubfileProgram <|-- DisplayFileFunction
    SubfileProgram <|-- EditFileFunction
    InteractiveProgram <|-- SingleRecordProgram
    SingleRecordProgram <|-- DisplayRecordFunction
    SingleRecordProgram <|-- EditRecordFunction

</pre>
