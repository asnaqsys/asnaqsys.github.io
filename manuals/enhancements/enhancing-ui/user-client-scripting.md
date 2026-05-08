---
title: "Extending Functionality with Client-side Scripting"
description: "Dive into client-side scripting basics. Perfect for developers looking to understand and leverage scripting in web applications."
---

Functionality of any [Expo Display Page](/concepts/user-interface/qsys-expo-display-pages.html) can be expanded using [JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript).

ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html) is written in [JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript) and provides support for common [User Interface](https://en.wikipedia.org/wiki/User_interface) operations for the Legacy Application and basic common modernization, for the Application to take advantage of Modern Web Browser's capabilities.

Most Applications will require further [User Interface](https://en.wikipedia.org/wiki/User_interface) enhancements tailored to their unique Application Domain and users. 

[HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) by definition is extensible, and the preferred Scripting Language is [JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript).

There are three areas which are typically extended thru the use of `Scripting`:
1. Function-Key Panel.
2. Visualization aids during operation of the page.
3. Quick Action shortcuts.

For the sake of this topic, we can also think of these three areas in the timing they affect the [User Interface](https://en.wikipedia.org/wiki/User_interface):

1. Right after the Page is loaded and **Initialized**.
2. During the operation of the Page.
3. Exit points to submit Actions to the server.

### Enhancing (or replacing) the Function-Key Panel

ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html) provides basic navigation panel with active Function Keys as defined by the [PageModel](/concepts/user-interface/razor-pages.html#pagemodel). The basic navigation consists of a Bar with named-links to submit the Page, sending the equivalent of keyboard [Command Key](https://www.ibm.com/docs/en/i/7.2?topic=80-cann-command-attention-keyword-display-files), to trigger an Action on the Application logic.

The only customization for the Page Navigation Panel presented by the [DdsFunctionKeys](/reference/expo/qsys-expo-tags/dds-function-keys-tag-helper.html) is the location:

1. `VerticalLeft` (default). 
2. `VerticalRight`.
3. `HorizontalTop`.
4. `HorizontalBottom`.
5. `Hidden`.

Expo Display Pages use a two panel with [Flex Display Layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) where one of the panels (or flex *item*) is used for the Active Function-Key Panel and the other for the *main* `DIV` where the input Form is rendered.

If the default layout is adequate for your Application, but needs some refinement, you can do it by:
1. Changing the CSS styles.
2. Writing `JavaScript` to add or modify the default HTML architecture.
3. Replace the Active Function-Key Panel with your own.

The first choice is done *statically*, by adding CSS to the Page (or globally to the file `~\wwwroot\css\site.css`). Standard Cascading style rules allow to override any style provided by default.

The other two choices are done *dynamically* each time the Page is rendered, using JavaScript and fall into the category *Right after the Page is loaded and **Initialized***, listed above.

Both choices (2 and 3), need to start running at a particular time in the Rendering cycle, explained below.

### When is the Expo Display Page "Loaded and Initialized"?

Knowing when the *Right after the Page is loaded and **Initialized*** event happens, when your Script should run, is a bit tricky. Thankfully, we are providing here [boilerplate code](https://en.wikipedia.org/wiki/Boilerplate_code) that you can paste into your Script. 

First you need to decide if the Script you need is to be applied *Globally* (for All pages), or just on a Page-per-Page basis.

If the Script is *Global*, it should be added to `~\Site\Pages\Shared\_Layout.cshtml`.

If the Script is *Local* to a Page, then it should be added to the `Script` section of a Page (common practice is to add it to the bottom of the page).

`_Layout.cshtml:`

```html
.
.
.

<body>
    @RenderBody()

    <script type="module">
        import { Page } from '../lib/asna-expo/js/asna.js';

        Page.init({ formId: 'MonarchForm' });
    </script>

    <script>
        // This User-Defined Script runs on ALL Pages.
        document.addEventListener('DOMContentLoaded', () => {
            console.log('~\\Pages\\Shared\\_Layout.cshtml Script running!');
        });
    </script>

    @RenderSection("Scripts", required: false)
</body>
```

<br>

`MYPAGE.cshtml:`

```html
.
.
.
    </DdsFile>
</form>

@section Scripts{
    <script>
        // This script runs on this Page only.
        document.addEventListener('DOMContentLoaded', () => {
            console.log('Page MYPAGE.cshtml Script Running!');
        });
    </script>
}
```

>The Best Practice is to add your Script after the [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) has completed its own processing.  

In addition to the [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction), ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html), needs to perform basic Page initialization execution.

>For now on, we will assume you want your Script to be *Global*.

ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html) uses a simple technique to indicate that the Page has been initialized: It changes the class for the element:

From:

```html
    <main role="main" class="display-element-uninitialized">
```

To:

```html
    <main role="main" class="display-element-initialized">
```

We can use Script logic to detect when the `class="display-element-uninitialized"` is no longer present in our `main` element. (Most Browsers on modern PC will run this code in less than one second.)

First, we need to find our [form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form) element, then inside the form, we need to find our `main` element.

```html
    <script>
.
.
.
    const form = document.querySelector('form[id="MonarchForm"]');
    if (form) {
        const main = form.querySelector('main[role=main]');
        if (main) {
            // We found our main! (where we want to look for the `uninitialized` class).
        }
    }

.
.
.
    </script>
```

>The `id` needs to match the `ID` given to the `form` element in the Expo Display Page.


The last Step is to use a standard [delay](https://developer.mozilla.org/en-US/docs/Web/API/setInterval) mechanism to wait for the `main` element to have its initial class `display-element-uninitialized` *removed*. Signaling the time when our Script can safely run.

Here is the complete [boilerplate code](https://en.wikipedia.org/wiki/Boilerplate_code):

```html
    <script>
        // This User-Defined Script runs on ALL Pages.
        document.addEventListener('DOMContentLoaded', () => {
            console.log('~\\Pages\\Shared\\_Layout.cshtml Script running!');
            const form = document.querySelector('form[id="MonarchForm"]');
            if (form) {
                const main = form.querySelector('main[role=main]');
                if (main) {
                    const wait = setInterval(() => {
                        if (!main.classList.contains('display-element-uninitialized')) {
                            console.log('~\\Pages\\Shared\\_Layout.cshtml detected Page initialized!');
                            clearInterval(wait);
                        // Add your own script code here!


                        }
                        else {
                            console.log('~\\Pages\\Shared\\_Layout.cshtml waiting on Page initialization ...');
                        }
                    }, 500);
                }
            }
        });
    </script>
```

>The `console.log` may be removed. Added here to enable `Tracing` inside Browser Developer's Tool `Console` output window. 

### When replacing the Panel, how do you obtain the Active Function-Keys?

If the [DdsFunctionKeys](/reference/expo/qsys-expo-tags/dds-function-keys-tag-helper.html) is chosen with its `location` property with the value 'Hidden', there is a simple [API](https://en.wikipedia.org/wiki/API) that can be used to retrieve the Application's *Active Function Keys* for the Page.

The [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) allows *global* definition of symbols accessible to any JavaScript function. Any object may be added as a property to the global [window](https://developer.mozilla.org/en-US/docs/Web/API/Window) object.

ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html) creates a *global* object called `asnaExpo` which gives access to essential functions and a few handy data-structures (JavaScript *objects*).

One of this objects, `activeFunctionKeys` provides information to re-build the `Hidden` *Active Function Keys*.

By adding the following code to your Script:

```html
    <script>
.
.
.
        if (window.asnaExpo.page && window.asnaExpo.page.activeFunctionKeys) { // For example, list the Active Function Keys (DdsFunctionKeys that was Hidden)
            console.log(`${window.asnaExpo.page.activeFunctionKeys.length} Active Function Keys:`);
            console.log(window.asnaExpo.page.activeFunctionKeys);
        }

    </script>
```

>When referring to attributes of `window`, it is not necessary to include the `window.` prefix. JavaScript assumes that *global* symbols should be looked up in the `window` object. `asnaExpo` or `asnaExpo.page` is enough syntax to refer to these objects.

Running your Application with any *Expo Display Page* rendered, will produce the following output on the Browser's Developers `Console`:

```
~\Pages\Shared\_Layout.cshtml Script running!
~\Pages\Shared\_Layout.cshtml detected Page initialized!
5 Active Function Keys:
Array(5)
    0: {title: 'Enter', text: 'Enter', pushKeyParms: {…}}
    1: {title: 'F3 - Exit', text: 'Exit', pushKeyParms: {…}}
    2: pushKeyParms: 
        fieldValue: ""
        focusElement: ""
        key: "F9"
        virtualRowCol: ""
        [[Prototype]]: Object
        text: "Spooled Files"
        title: "F9 - Spooled Files"
        [[Prototype]]: Object
    3: {title: 'PageUp', text: 'PageUp', pushKeyParms: {…}}
    4: {title: 'PageDown', text: 'PageDown', pushKeyParms: {…}}
    length: 5
    [[Prototype]]: Array(0)
```

Regarding **activeFunctionKeys** object, it is defined as an array of:

```cs
    {
        "text"  : string,   // Used as button text
        "title" : string,   // Used as tooltip text
        pushKeyParms: {
            "key"           : string,    // IBMi aid key
            "focusElement"  : string,    // Model's field name.
            "fieldValue"    : string,    // Field value (as if it had been typed by user)
            "virtualRowCol" : string     // Legacy row,col screen position (possibly tested by Application logic to identify input)
        }
    }
```

`text` and `title` property values should be straightforward (when designing the new Options Panel). The `pushKeyParms` are the values needed when implementing `click` event handler (or equivalent), to submit the Command `Action` to the Application server.

<br>

### The *Proper* way to submit a Page "Action" Request

The most important [API](https://en.wikipedia.org/wiki/API) object exposed by ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html) is access to the `pushKey` function.

```cs
 pushKey(aidKeyToPush, focusElementName, fieldValue, virtualRowCol) {

 }
```

Using the `pushKeyParms` of one of the elements of the array above, you would want to add the following code to your `click` event handler:

```html
<script>

    let action = asnaExpo.page.activeFunctionKeys[2]; // This is for illustration purposes only. Real code depends on how you captured the data.

    asnaExpo.page.pushKey( action.pushKeyParms.key, 
                           action.pushKeyParms.focusElement, 
                           action.pushKeyParms.fieldValue, 
                           action.pushKeyParms.virtualRowCol );

</script>
```

<br>

Notes:
1. The only required parameter is the first one: `key`.
2. `key` is a string representation of one of these [AidKey](/reference/expo/qsys-expo-model/aid-key.html).
3. There are two exceptions: AidKey.PageUp is represented by `"PgUp"` and AidKey.PageDown by `"PgDn"`.
4. The parameters: `focusElementName`, `fieldValue`, `virtualRowCol` are optional.
5. Calling `pushKey` runs code to prepare submission (setting internal input-hidden elements to values expected by the server - i.e. feedback information). `pushKey` saves the Page as an image in [Session storage](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage) entries to be used by `WINDOW` (modal display background image) on subsequent pages. Lastly, `pushKey` prepares an animation to show a *Wait* cursor while the request is serviced.
6. `pushKey` can be called at any time (in addition to Menu option's `click` handlers).
7. `pushKey` call *does not* return. Shortly after the call is made, the Page is removed from the DOM.

<br>

### Advanced Expo Client Callbacks to User-defined code.

So far we have described how to *Use* ASNA [Expo Client Library](/concepts/user-interface/qsys-expo-client-library.html) functionality from User-defined Scripting.

There are some events while `Expo Client Library` is executing its code, where it wants to *talk* to User-defined Scripting code. These are called `hooks` or `Notification callback` functions.

The following lists `Expo Client Library` callbacks:

| Function Name              | Description                                                          | Typical uses                                         |
|----------------------------|----------------------------------------------------------------------|------------------------------------------------------|
| MonarchPageSavingForPopup  | Called right before the Page will be saved for future WINDOW Page    | When DOM needs to be changed before saving.          |
| MonarchPageForPopupSaved   | Called right after the Page has been saved (for future WINDOW Page)  | When DOM needs to be cleaned-up after saving.        |
| MonarchSubfilePageChanging | Called right before AJAX response will change a subfile.             | Rarely used.                                         |
| MonarchSubfilePageChanged  | Called right after a subfile rows have been changed by AJAX response.| To re-apply event handlers that might have been lost.|
| MonarchWindowBackgroundHtmlToImageFilter  | A node is passed. Return *true* to include, *false* to exclude.| Filter-out elements when saving Page (as background for next) |

All you need to do is implement any of the `Notification callback` functions in your Script code, and `Expo Client Library` will call it when it needs to.

>All `Notification callback` functions are optional.

