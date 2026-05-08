---
title: "BTerm Macros"
description: "Learn to automate tasks in BTerm with macros. This guide provides easy steps to create, manage, and use macros for efficiency."
---

The ASNA 5250 Terminal Emulator code provides a function that accepts an array of Actions and/or characters, and executes each in the sequence specified by the array positions.

The function is called:

```javascript
WingsTerminal.executeMacro(macro);
```

where, macro is an instance of an array of strings, with elements containing names of Actions or, if the length of the string is one, the string is used as a character to be processed by the emulator as if it were entered directly from the keyboard. There is no need to indicate Shift, Control, or Alt on keystrokes, since the Actions produced by such combinations can be requested directly.

The first string in the array is reserved for the name of the macro.

## Example

Let's assume that we want a macro to execute the following steps.

1. Move the cursor to the first field and position one (Record Home).
2. Enter 'ADDLIBLE NUTSNBOLTS' (Add Library List Entry NUTSNBOLTS).
3. Submit page with 'Enter' `Aid key`.

```html
<button type="button" onclick= "return testMacro();">Add Libl Entry Macro</button>
```

The implementation of the testMacro() JavaScript function is as follows:

```html
<script>
    const testMacro = () => {
        const macro = [
            'Test Macro', // The name of the Macro (ignored during execution)
            'RECORD',     // First action, goto Home position
            'A', 'D', 'D', 'L', 'I', 'B', 'L', 'E', ' ',
            'N', 'U', 'T', 'S', 'N', 'B', 'O', 'L', 'T', 'S',
            'ENTER' 
            ];

        WingsTerminal.executeMacro(macro);
        return false;        
    }
</script>
```

Notice how the array contains two `Actions``: **'RECORD'** and **'ENTER'**, which are both case sensitive.
These are two of the actions listed in [Keyboard Mapping](./bterm-keyboard-mapping.html). 
**'RECORD'** moves the cursor to the Home position and **'ENTER'** submits the page with an `QSN_ENTER` (0xf1) Aid key. 

The rest are letters that are typed to fill the input field (`ADDLIBLE` and `NUTSNBOLTS`). 

Once the macro array has been declared, all we need to do is call the WingsTerminal.executeMacro function with the macro as the only parameter. 

Lastly, returning false to the onclick event prevents it from executing any further actions.

## Macros are Interrupted after Submitting a Page

The macro is interrupted when it executes any `Action`` that causes the Page to be submitted because of the Stateless behavior of Web applications. 

In fact, the JavaScript that implements the 5250 Terminal Emulator, as well as any JavaScript in the page, is released from memory and re-loaded when the request is returned.

There are advanced techniques that can be implemented to split a large macro into segments, divided by submitting Actions and those that are to be continued the next time the page renders again, which could also contain submitting Actions.

These techniques involve storing the macro in a file (or local storage) as well as the state regarding the segments already executed. 
A hidden field may be added to the page with the segment of the macro to be executed the next time; and the JavaScript can control the subsequent segments to be executed. ~/Themes/Current/`~\Pages\Terminal\Terminal.cshtml.cs` model may be altered to accomplish these steps.

