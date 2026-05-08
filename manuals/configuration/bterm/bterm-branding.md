---
title: "BTerm Branding"
description: "Elevate your brand with our BTerm branding guidelines. Learn to apply our visual and verbal identity principles for maximum impact."
---

## Changing Color and/or Background Defaults

The end user is able to change the colors of the Terminal Emulator using the Change Colors option, but in order to modify the defaults, changes should be made to the CSS file `5250.css`

The CSS file `5250.css` is part of Expo JavaScript library:

```
~\wwwroot\lib\asna-expo\css\5250.css
```

The following styles in `5250.css` set the default colors:

```css
/* Terminal Color defaults */
.AsnaTermDEF_GREEN     { color: #00FF00; }
.AsnaTermDEF_BKGD      { color: #000000; }
.AsnaTermDEF_BLUE      { color: #0099FF; }
.AsnaTermDEF_RED       { color: #FF0000; }
.AsnaTermDEF_WHITE     { color: #FFFFFF; }
.AsnaTermDEF_TURQUOISE { color: #AFEEEE; }
.AsnaTermDEF_YELLOW    { color: #FFFF00; }
.AsnaTermDEF_PINK      { color: #FF1493; }
.AsnaTermDEF_CURSOR    { color: #FFFFFF; }
.AsnaTermDEF_SEL       { color: #FFFFFF; }
```

Modifying the colors in the .css will alter the defaults, but end users can still modify the colors locally using the options on the **color picker** panel. End users can also reset to the defaults by clicking the "Restore Defaults" button on the color picker.

In the event of a conflict or one of the colors being absent in `5250.css`, the terminal emulator will fall back on the colors defined the client's local storage, as outlined in the following table:

| Item key | Default value |
| :- | :- |
| ASNA.5250Terminal.greenColor | '#00FF00' |
| ASNA.5250Terminal.blackColor | '#000000'|
| ASNA.5250Terminal.blueColor | '#0099FF' |
| ASNA.5250Terminal.redColor | '#FF0000' |
| ASNA.5250Terminal.whiteColor |'#FFFFFF'|
| ASNA.5250Terminal.turquoiseColor | '#AFEEEE' |
| ASNA.5250Terminal.yellowColor |'#FF1493'|
| ASNA.5250Terminal.pinkColor | '#FF1493' |
| ASNA.5250Terminal.backgroundColor | '#000000' |
| ASNA.5250Terminal.cursorColor| '#FFFFFF' |
| ASNA.5250Terminal.selectColor | '#FFFFFF' |
| ASNA.5250Terminal.menubarTextColor | #000000' |
| ASNA.5250Terminal.menubarColor | '#FFFFFF' |
| ASNA.5250Terminal.menubarBackgroundImage | 'url(Images/menubar_terminal_default.jpg)' |
| ASNA.5250Terminal.menubarBackgroundRepeat | 'repeat-y' |
| ASNA.5250Terminal.statusbarTextColor | '#000000' |
| ASNA.5250Terminal.statusbarColor | '#FFFFFF' |
| ASNA.5250Terminal.statusbarBackgroundImage | 'url(Images/statusbar_terminal_default.jpg)'|
| ASNA.5250Terminal.statusbarBackgroundRepeat | 'repeat-y' |
| ASNA.5250Terminal.backgroundRepeat | 'no-repeat' |
| ASNA.5250Terminal.menuColorsRedirectLocation | '5250ColorSchemas' |

## Overriding user color preferences.
User color preferences may be overriden, by changing the storage of the user preferences with hard-coded styles. This technique requires some JavaScript code lines before the Terminal is rendered.

1. Edit the ~\Pages\Terminal\Terminal.cshtml RazorPage.
2. Identify the JavaScript section at the bottom of the Terminal RazorPage.

```javascript
<script type="module">
    import { Terminal } from '../lib/asna-expo/js/bterm/terminal.js';

    Terminal.init()
        .then(
            () => Terminal.render( () => { return { width: window.innerWidth, height: window.innerHeight }; }
        )
    );
</script>
```

3. Add entries with your new defaults, **BEFORE** the call to the function `Terminal.init()`. The following example demonstrates the entries you could add.

```javascript
<script type="module">
    import { Terminal } from '../lib/asna-expo/js/bterm/terminal.js';

    const keyNamespace = 'ASNA.5250Terminal.';

    localStorage.setItem(keyNamespace + 'greenColor', newGreenDefault );
    localStorage.setItem(keyNamespace + 'blackColor', newBlackDefault );
    localStorage.setItem(keyNamespace + 'blueColor', newBlueDefault );
    localStorage.setItem(keyNamespace + 'redColor', newRedDefault );
    localStorage.setItem(keyNamespace + 'whiteColor', newWhiteDefault );
    localStorage.setItem(keyNamespace + 'turquoiseColor', newTurquoiseDefault );
    localStorage.setItem(keyNamespace + 'yellowColor', newYellowDefault );
    localStorage.setItem(keyNamespace + 'pinkColor', newPinkDefault );
    localStorage.setItem(keyNamespace + 'backgroundColor', newBackgroundColorDefault );
    localStorage.setItem(keyNamespace + 'cursorColor', newCursorColorDefault );
    localStorage.setItem(keyNamespace + 'selectColor', newSelectColorDefault );
    localStorage.setItem(keyNamespace + 'menubarTextColor', newMenubarTextColorDefault );
    localStorage.setItem(keyNamespace + 'menubarColor', newMenubarColorDefault );
    localStorage.setItem(keyNamespace + 'menubarBackgroundImage', newUrl );
    localStorage.setItem(keyNamespace + 'menubarBackgroundRepeat', newCSSRepeat );
    localStorage.setItem(keyNamespace + 'statusbarTextColor', newStatusTextColorDefault );
    localStorage.setItem(keyNamespace + 'statusbarColor', newStatusbarColorDefault  );
    localStorage.setItem(keyNamespace + 'statusbarBackgroundImage', newUrl );
    localStorage.setItem(keyNamespace + 'statusbarBackgroundRepeat', newCSSRepeat );
    localStorage.setItem(keyNamespace + 'backgroundImage', newImage );
    localStorage.setItem(keyNamespace + 'backgroundRepeat', newCSSRepeat );

    Terminal.init()
        .then(
            () => Terminal.render( () => { return { width: window.innerWidth, height: window.innerHeight }; }
        )
    );
</script>
```
