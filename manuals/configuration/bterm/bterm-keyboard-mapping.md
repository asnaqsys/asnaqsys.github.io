---
title: "BTerm Keyboard Mapping"
description: "Effortlessly customize your keyboard with BTerm mapping. This guide helps you tailor key functions for an optimized typing experience."
---

## 5250 Terminal Keyboard Mapping

## Default Keyboard Settings

The following keyboard 'actions' are identified and mapped to either an `IBM Aid key` that gets submitted or a terminal command to edit field content or to move the cursor position.

| Action | Description | Default Mapping | JavaScript Keycode | Comment |
| :- | :- | :- | :- | :- |
| `'ATTN'` | Alerts the host system that a requested function is not being honored.| Ctrl + F5 | Ctrl + 116 | Sets Bit 1 on [Telnet flags](./bterm-keyboard-mapping.html#telnet-flags) header field and submits the page to the IBM i.  Also accessible on the menu bar. |
| `'BEGIN'` | Place cursor at the start of field. | Ctrl + F9 | 120 | |
| `'CLEAR'` | Submit `QSN_CLEAR (0xbd)` to IBM i. | Scroll Lock | 145 | Also accessible on the menu bar. |
| `'COPY'` | Copy selected text to the Windows clipboard. | Ctrl + C IE Menu 'Copy'| String.fromCharCode(key.code).toUpperCase() == 'C' key.ctrlKey *true* | Context menus do not work. IE Browser Edit menu is supported. |
| `'CURSOR'` | Toggle between normal cursor and cross-hair cursor. | (None) | (None) | Cross-hair cursor not implemented. |
| `'CUT'` | Cut selected text (inside input capable field). | Ctrl + X IE Menu 'Cut'| String.fromCharCode(key.code).toUpperCase() == 'X' key.ctrlKey *true* | Context menus do not work. IE Browser Edit menu is supported. |
| `'DELETE'` | Delete character at cursor position. | Delete Del | 46 | JavaScript does not distinguish between 'Delete' and 'Del'. |
| `'DOWN'` | Move cursor one position down. | any Down Arrow | 40 | JavaScript does not distinguish between the different 'Down Arrow' keys on the keyboard. |
| `'DUP'` | If field has `DUP` attribute, the field is filled with the DUP characters from the cursor position. | Ctrl + F6 | (None) | |
| `'END'` | Place cursor at the end of a field. (Note: this is different from LAST, which positions the cursor at the last character entered into the field).| Ctrl + F11 | 122 | |
| `'ENTER'` | Submit `QSN_ENTER (0xf1)` to IBMi. | any Enter | 13 | JavaScript does not distinguish between the different 'Enter' keys on the keyboard. |
| `'ERASE'` | Clears all input fields and sets them to their default value. | (None) | (None) | Not mapped to a key. On the Menu bar. |
| `'F1' ... 'F24'` | Submit `QSN_F1 (0x31)... QSN_F24 (0xbc)` to IBMi. | F1 ... F12 Shift + F1 ... Shift + F12| 112 ... 123 Shift + 112 ... Shift + 123| |
| `'FASTDOWN'` | Move cursor three positions down. | Ctrl + Down Arrow | 40 key.ctrlKey *true* | |
| `'FASTLEFT'` | Move cursor three positions left. | Ctrl + Left Arrow | 37 key.ctrlKey *true* | |
| `'FASTRIGHT'` | Move cursor three positions right. | Ctrl + Right Arrow | 39 key.ctrlKey *true* | |
| `'FASTUP'` | Move cursor three positions up. | Ctrl + Up Arrow | 38 key.ctrlKey *true* | |
| `'FIELDMINUS'` | Erase the rest of the field and move the cursor to the next field. For numeric fields, change the sign to negative. | Shift + - *(numeric keypad)* | (None) | Not mapped to any key. | 
| `'FIELDPLUS'` | Erase the rest of the field and move the cursor to the next field. For numeric fields, change the sign to positive. | Shift + + *(numeric keypad)* | (None) | 	Not mapped to a key. |
| `'FIELDEXIT'` | Erase the rest of the field and move the cursor to the next field. | Shift + Enter | (None) | Not mapped to a key. |
| `'FIELDEXITENTER'` | Justify the field and send the ENTER command to the IBM i. | Ctrl + Enter | 13 key.ctrlKey *true* | |
| `'HELP'` | Help in error state. When input validation fails, error codes are set and a help on error request is sent to the IBM i. | (None) | (None) | Not mapped to a key. Sets Bit 7 on Telnet flags header field. Sets error code in 5250 data stream and submits the page to the IBM i. Also accessible on the menu bar. |
| `'HEX'` | Shows a dialog where Hex can be typed to enter a character not on the keyboard. If only one character is entered, the character will be taken verbatim. | (None) | (None) | Not mapped to a key. Accessible on the menu bar. |
| `'INSERT'` | Toggle insert mode. | Insert Ins | 45 | |
| `'LAST'` | Jump to the last character of a field. | any End | 35 | |
| `'LEFT'` | Move cursor one position left. | any Left Arrow | 37 | JavaScript does not distinguish between the different 'Left Arrow' keys on the keyboard. |
| `'LEFTDELETE'` | Delete character left of the cursor. | Backspace | 8 | |
| `'NEWLINE'` | Jump to next line | Shift + Enter | 13 key.shiftKey *true* | |
| `'NEXT'` | Jump to the next field. | Tab | 9 | |
| `'PASTE'` | Copy the contents of the Clipboard to the current cursor's position. | Ctrl + V (IE 'Paste' menu) | | |
| `'PGDN'` | Roll *UP* the screen | Page Down | | |
| `'PGUP'` | Roll *DOWN* the screen | Page Up | | |
| `'PREVIOUS'` | Jump to the previous field. | Shift + Tab | 9 key.shiftKey *true* | |
| `'PRINT'` | Submit `QSN_PRINT (0xf6)` to the IBMi. | (None) | (None) | Not mapped to a key. |
| `'RECORD'` | Record Backspace (Home). Put cursor at the Home position (first input field, position 1). | any Home | 36 | JavaScript does not distinguish between the different 'Home' keys on the keyboard. |
| `'RESET'` | Opens the keyboard for input (if keyboard is LOCKED due to error). | Esc | 27 | [May be re-mapped](./bterm-keyboard-mapping.html#customizing-the-keyboard) to Ctrl + R |
| `'REDIRECT:Page'` | Navigate to new Page | (None) | (None) | Page is relative to the location of the `Terminal.cshtml`. It could specify a folder but make sure to provide a way to get back to the `~\wwwroot\Pages\Terminal\Terminal.cshtml` page. |
| `'RIGHT'` | Move cursor one position right. | any Right Arrow | 39 | JavaScript does not distinguish between the different 'Right Arrow' keys on the keyboard. |
| `'SYSREQ'` | System request interrupt. | Shift + Esc Ctrl + F4 | (None) | Not implemented. |
| `'UP'` | Move cursor one position Up. | any Up Arrow | 38 | JavaScript does not distinguish between the different 'Up Arrow' keys on the keyboard. |

## Telnet Flags

A few of the 'Actions' that submit but do not send Aid Key to the IBM i need to effect the Telnet message header instead. According to http://www.ietf.org/rfc/rfc1205.txt, there is a 16 bit flag field in the Telnet header. Eight of those bits are reserved and should be set to zero.

| Bit |  | Description | 
| :-: | :- | :- |
| 0 | ERR | This bit is set to indicate a data stream output **error**. The negative response code is sent as data following the op code field.|
| 1 | ATN | This bit is set to indicate that the 5250 **attention key** was pressed. |
| 2, 3, 4| * | These bits are reserved (set to zero). |
| 5 | SRQ | This bit is set to indicate that the 5250 **System Request key** was pressed. |
| 6 | TRQ | This bit is set to indicate that the 5250 **Test Request key** was pressed. |
| 7 | HLP | This bit is set to indicate the Help in Error State function. The error code is sent as data following the header and is a four digit packed decimal number. For example, an error code of '0005'X indicates the operator attempted to type in an area of the display that is not enabled for input. |
| 8 thru 15| * | These bits are reserved (set to zero). |





## Customizing the Keyboard
To map Actions not set by default or to customize keyboard mapping, you can add a few lines of JavaScript code to the `~\Pages\Terminal\Terminal.cshtml` RazorPage.

The JavaScript code that implements the ASNA 5250 Terminal emulator subscribes to the following browser events:

```
document.body.onkeydown
document.body.onkeypress
```

When keyboard input is identified, the input is normalized into a Key object with the following properties:

```javascript
Key = (code, ctrlKey, altKey, shiftKey) => {
      this.code     = code;
      this.ctrlKey  = ctrlKey;
      this.altKey   = altKey;
      this.shiftKey = shiftKey;
   }
```

This Key object needs to be mapped into either an `Action`, as noted above, or a `character` to be added to the field at the cursor's position. Before applying the Defaults above, the ASNA 5250 Terminal emulator JavaScript code checks for the global function `WingsTerminalMapKey`. If it exists as a function, then it is called with the following parameters:

| Parameter | Description | 
| :- | :- |
| inputKey | **Key object** described above with the properties populated with information from the Browser event that caused it. |
| wasKeyPress | Boolean indicating the origin of the input. *True* if the event originated from onkeypress, *False* if the event originated from `onkeydown`. |
| outEvent | [Input event object instance](./bterm-keyboard-mapping.html#input-event-object-instance) |

### Input event object instance

This is the object we need to change to indicate the mapping. the two properties are:

```javascript
InputEvent = function ( action, character) {
   this.action = action;
   this.character = character;
}
```

Where action should be assigned a string value and character should be assigned a string value with one character to be added at the cursor's position (if positioned at an input field).

Only one of the properties should be changed unless that key event should be processed by the default action or character.

## Keyboard Mapping example

For example, the following implementation of global function WingsTerminalMapKey will map the 'RESET' action to the Ctrl + R key combination. Note: the default 'Esc' mapping would still work. To disable the default code, map it to a blank action.

## Adding Hot-keys for International Characters

When an international character is not available on the keyboard, it is still possible to produce the symbol adding some customization. 

Even the numeric keypad (when Num Lock is ON), may be used to enter characters – giving its ascii code. For example, Alt 164 on US keyboard produces the 'ñ' symbol - it may be simpler to remember to produce these, by a combination with the Ctrl key. You can easily map 'ñ' or accent on vowels with a sequence such as Ctrl, like in the following example:

```html
<script type="text/javascript">
   WingsTerminalMapKey = (inputKey, wasKeyPress, outEvent) => {
      if ( inputKey.ctrlKey ) {
         switch( String.fromCharCode(inputKey.code).toUpperCase() ) {
            case 'N' :
               outEvent.character = 'ñ';
            break;
            case 'A' :
               outEvent.character = 'á';
            break;
            case 'E' :
               outEvent.character = 'é';
            break;
            case 'I' :
               outEvent.character = 'í';
            break;
            case 'O' :
               outEvent.character = 'ó';
            break;
            case 'U' :
              outEvent.character = 'ú';
            break;
         }
      }
   }
</script>
```
