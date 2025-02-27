---
title: "Hamburger Menu navigation: Prompt to replace Function Key Banner."
description: "Learn to write effective AI Prompt to generate code to replace Application Function Key Banner with a Hamburger Menu."
---

### The prompt wrote JavaScript to replace the standard Function-key Banner produced during Migration, and replaced it with a [Hamburger Menu](https://apix-drive.com/en/blog/ecommerce/hamburger-menu-definition).


<style>
pre {
  white-space: pre-wrap; /* Wraps the text */
  word-wrap: break-word; /* Prevents overflow */
}
</style>

<pre>The Website project #&lt;reference-to-csproj-file-in-my-solution&gt; renders several pages (driven by the application-logic). 
All of the pages present a Banner that shows buttons that represent active Aid-keys. 

The Banner is rendered as a NAV html element, that uses a class whose name starts with 'dds-activekey-'. 

Inside the generated HTML element a collection of anchor elements (role=button) are rendered for each Aid-key that is active on that Page. 
The 'title' property has the label of the key name. 
Each button will get at runtime a 'Click' event handler with the appropriate function handler code to execute a runtime passing pre-determined parameters. 

Please write JavasScript code to run after the Page completed rendering, that will locate the Banner, identify the inner buttons, and create a Hamburger menu - with a nicer Font family and smaller font height - that will present menu options for the original buttons preserving labels and Click event handling code. The Hamburger should be added as the first child of the element 'main[role=main]', while the original Banner should hide (not removed). The new JavaScript should be added to 'wwwroot\js' and the related CSS to 'wwwroot\css\site.css'
</pre>

<style>
pre {
  white-space: pre
  word-wrap: normal
}
</style>

### The prompt suggested the following changes

*Sure, let's start by creating the JavaScript code to handle the Hamburger menu functionality. We'll place this code in a new file called wwwroot/js/hamburgerMenu.js.*

```js
document.addEventListener("DOMContentLoaded", function () {
    // Locate the Banner
    const banner = document.querySelector("nav[class^='dds-activekey-']");
    if (!banner) return;

    // Identify the inner buttons
    const buttons = banner.querySelectorAll("a[role='button']");
    if (buttons.length === 0) return;

    // Create the Hamburger menu
    const hamburgerMenu = document.createElement("div");
    hamburgerMenu.className = "hamburger-menu";
    const menuButton = document.createElement("button");
    menuButton.className = "hamburger-button";
    menuButton.innerHTML = "&#9776;"; // Hamburger icon
    const menuContent = document.createElement("div");
    menuContent.className = "hamburger-content";

    // Add buttons to the Hamburger menu
    buttons.forEach(button => {
        const menuItem = document.createElement("a");
        menuItem.href = "#";
        menuItem.textContent = button.title;

        // Preserve click handlers
        menuItem.addEventListener('click', function (event) {
            event.preventDefault();
            button.click();
        });

        menuContent.appendChild(menuItem);
    });

    hamburgerMenu.appendChild(menuButton);
    hamburgerMenu.appendChild(menuContent);

    // Add the Hamburger menu as the first child of the main element
    const mainElement = document.querySelector("main[role='main']");
    if (mainElement) {
        mainElement.insertBefore(hamburgerMenu, mainElement.firstChild);
    }

    // Toggle menu visibility on button click
    menuButton.addEventListener("click", function (event) {
        event.preventDefault();
        menuContent.classList.toggle("show");
    });

    banner.style.display = "none";
});
```


*Next, let's add the related CSS to wwwroot/css/site.css to style the Hamburger menu.*



```css
/* Hamburger menu styles */
.hamburger-menu {
    position: relative;
    display: inline-block;
}

.hamburger-button {
    font-family: Arial, sans-serif;
    font-size: 16px;
    background-color: #333;
    color: white;
    border: none;
    cursor: pointer;
    padding: 10px;
}

.hamburger-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
}

.hamburger-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    font-family: Arial, sans-serif;
    font-size: 14px;
}

.hamburger-content a:hover {
    background-color: #f1f1f1;
}

.hamburger-content.show {
    display: block;
}
```

*Finally, ensure that the new JavaScript file is included in your HTML layout. You can add the following script tag to your main layout file (e.g., _Layout.cshtml if using Razor)*:

```html
<script src="~/js/hamburgerMenu.js"></script>
```

*This setup will create a Hamburger menu that appears as the first child of the main element, preserving the labels and click event handlers of the original buttons.*

<br>

### How Copilot Helps with Writing Code

Even small changes assume you remember many details about JavaScript and CSS (or perhaps it generated code you thought was beyond your reach). Using the prompt definitely saves time.

### Reflections and Next Steps

The prompt contains details requiring knowledge of how the [Monarch Expo](/manuals/enhancements/enhancing-ui/user-client-scripting.html) works. If the provided code doesn't work on the first try, you can always ask for more details and provide more references to your code. AI is ready to work in your context. If the new code produces build errors, you can copy from the log output and ask AI for assistance.

If there's a particular detail you don't like, such as font style, sizes, or the location of the Hamburger button, you can modify the provided prompt and ask AI to try again.

## Results

| Before | After |
| :-: | :-: |
| ![Before](../images/original-banner.png) | ![After](../images/banner-replaced-hamburger-menu.png) |
