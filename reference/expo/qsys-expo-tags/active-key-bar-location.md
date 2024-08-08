---
title: "ActiveKeyBarLocation enum     | QSYS API Reference Guide"
description: "Specifies the Active Function Key Bar location and direction. "
last_modified_at: 2024-08-08T21:42:22Z
---

Specifies the Active Function Key Bar location and direction.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll
<br>
<br>

## Remarks

Consistent with [DDS for display files](https://www.ibm.com/docs/en/i/7.1?topic=dds-display-files), QSys Expo Display Pages define an [HTML form element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form) with a [DdsFile Tag Helper](/reference/expo/qsys-expo-tags/dds-file-tag-helper.html) child element which represents the root structure of the Page.

As shown below, a simplified (and collapsed) markup structure, the [DdsFile](/reference/expo/qsys-expo-tags/dds-file-tag-helper.html) Tag Helper has two elements:

1. A [DdsFunctionKeys](/reference/expo/qsys-expo-tags/dds-function-keys-tag-helper.html) Tag Helper.
2. A [main HTML element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main).

> The rest of the DdsXXX Tag helpers, like [DdsRecord](/reference/expo/qsys-expo-tags/dds-record-tag-helper.html), [DdsSubfileControl](/reference/expo/qsys-expo-tags/dds-subfile-control-tag-helper.html) Tag Helper and [DdsMessagePanel](/reference/expo/qsys-expo-tags/dds-message-panel-tag-helper.html) Tag Helper, are described inside the [main HTML element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main).

```html
<form id="MonarchForm" method="post">
    <DdsFile DisplayPageModel="Model">

        <DdsFunctionKeys Location="HorizontalBottom" />
        
        <main role="main">
            <DdsSubfileControl>...<DdsSubfileControl>
            <DdsRecord>...</DdsRecord>
        </main>
    </DdsFile>
</form>
```

Typically, the first Tag Helper described inside the [DdsFile](/reference/expo/qsys-expo-tags/dds-file-tag-helper.html) Tag Helper is the [DdsFunctionKeys](/reference/expo/qsys-expo-tags/dds-function-keys-tag-helper.html) Tag Helper.

The [DdsFunctionKeys](/reference/expo/qsys-expo-tags/dds-function-keys-tag-helper.html) Tag Helper determines how the collection of `Active Function Keys` will be rendered as clickable buttons.

> Notice that selecting the Location of the `Active Function Keys` also determines where the rest of the Page (main elements) will be rendered. I.E. if the `Location` is **Hidden**, the `main` elements will be rendered as a full-page, if the `Location` is **HorizontalTop**, the `main` elements will be rendered below the `Active Function Keys` horizontal bar, in the same way, if the `Location` is **HorizontalBottom**, the `main` elements will be rendered above the `Active Function Keys` horizontal bar, etc. 

The `ActiveKeyBarLocation Enumeration` has the possible values for the `Location` property for the [DdsFunctionKeys](/reference/expo/qsys-expo-tags/dds-function-keys-tag-helper.html) Tag Helper.


## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Hidden | Keys are not rendered . | 4 |
| HorizontalBottom | Keys are rendered in a horizontal direction on the bottom of the page. | 3 |
| HorizontalTop | Keys are rendered in a horizontal direction on the top of the page. | 2 |
| VerticalLeft | Keys are rendered in a vertical direction on the left of the page. | 0 |
| VerticalRight | Keys are rendered in a vertical direction on the right of the page. | 1 |
