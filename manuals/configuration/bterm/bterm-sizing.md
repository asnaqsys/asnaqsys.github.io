---
title: "BTerm Sizing"
description: "Enhance your workflow with our guide on BTerm window sizing. Learn to adjust and optimize window dimensions for maximum efficiency."
---

## Changing the Terminal Display Size

The initial size of the Terminal Emulator window is controlled by the entry-point Javascript function (WingsTerminal.render) called right after the `~\Pages\Terminal\Terminal.cshtml` RazorPage gets loaded.

The script that controls it is:

```html
<script type="module">
    import { Terminal } from '../lib/asna-expo/js/bterm/terminal.js';

    Terminal.init()
        .then( () => 
            Terminal.render( () => { 
                return { width: window.innerWidth, height: window.innerHeight }; 
            }
        )
    );
</script>
```

The WingsTerminal.render function takes one parameter, which can be either:

1. An object with two properties: width and height (see fixed size below). These properties have numeric values (in pixels) representing the size of the `<div>` where the 5250 screen will be presented. Given the size in pixels, an appropriate font height will be selected to show exactly the number of rows contained in the 5250 screen (24 or 27, depending on the Terminal's screen size).
Or,
2. A function that will be called by the Emulator's rendering engine whenever the current size is required to paint the page.

## Setting a Fixed Size

Setting the Terminal Emulation window to a static size is quite simple: If the WingsTerminal.Render function is passed an unnamed object, by simply listing the height and width properties using the JavaScript syntax, the renderer will dynamically create an object, like in the following example:

```javascript
    Terminal.render( () => { 
        return { width: 960, height: 720 }; 
    }
```

## Setting an Adjustable Size

