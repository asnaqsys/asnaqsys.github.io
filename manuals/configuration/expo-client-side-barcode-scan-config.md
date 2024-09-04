---
title: "Expo for Monarch Apps: Client-Side Barcode Scanning Config."
description: "Master Expo for Monarch app development. Learn to manage client-side content with additional support for Barcode Scanning."
---

## Barcode Scanning on devices with camera

Modern computers and Mobile Devices, can effectively use their cameras to scan barcodes, functioning similarly to traditional barcode scanner guns. Here’s how it works:

1. **Camera Activation**: When you activate (tap of click on the button next to the [DdsBarcodeField](/reference/expo/qsys-expo-tags/dds-barcode-field-tag-helper.html) ), the camera is activated to capture video looking for a clear image including the full barcode.

2. **Image Capture**: The camera captures an image of the barcode. This image includes the pattern of black and white bars (or squares in the case of QR codes).

3. **Image Processing**: The JavaScript processes the captured image. It identifies the barcode within the image by detecting the contrast between the black and white areas. If the capture image is not recognized, Step 2 is repeated.

4. **Decoding**: The app then decodes the barcode. It translates the pattern of bars into a digital format, typically a series of numbers or letters. This is done using algorithms that interpret the width and spacing of the bars.

5. **Data Retrieval**: The decoded information is then pasted into the [DdsBarcodeField](/reference/expo/qsys-expo-tags/dds-barcode-field-tag-helper.html) value. When the Page is submitted, the Application logic will use the decoded code to retrieve data. For example, it might pull up product details, prices, or URLs if it’s a QR code, etc.

## Camera capabilities required

For device equipped with a camera to effectively scan barcodes, the camera should have certain key features:

1. **Resolution**: A camera with at least 8-12 megapixels is generally sufficient for most barcode scanning tasks. Higher resolution cameras (16MP or more) can be beneficial for scanning very small or densely packed barcodes.

2. **Autofocus**: Good autofocus capabilities are crucial. This ensures that the camera can quickly and accurately focus on the barcode, even if it’s close up or at an angle.

3. **Low Light Performance**: A camera that performs well in low light conditions is important, as barcodes might need to be scanned in various lighting environments. Features like a larger aperture (e.g., f/1.8) and image stabilization can help.

4. **Macro Capabilities**: For scanning very small barcodes, a camera with good macro capabilities is beneficial. This allows the camera to focus on objects that are very close to the lens.

5. **Shutter Speed and Image Stabilization**: A camera with a fast shutter speed and image stabilization helps prevent blurring, which is especially useful if the barcode or the device is moving3.

## Open-source JavaScript Library to Scan Barcodes.

ASNA Monarch Expo Client Library relies on [ZXing ("zebra crossing") Javascript](https://github.com/zxing-js) Open Source Project.

>Note: `ZXing` is a rather large library, which **is not** configured by default for sites created with the standard templates. 

If your site has at least one Displayfile Pages that includes the [DdsBarcodeField](reference/expo/qsys-expo-tags/dds-barcode-field-tag-helper.html), the following files on your site need to be updated:

1. `~\Site\Pages\Shared\_Layout.cshtml` - Layout master page for all Displayfiles on your site.

2. `~\Site\libman.json` - The [LibMan](https://learn.microsoft.com/en-us/aspnet/core/client-side/libman/libman-vs?view=aspnetcore-8.0) JSON configuration file that determines the JavaScript libraries that are downloaded into your site.

## _Layout.cshtml additions.

Before a Displayfile Page is sent to the Browser when a Request comes into you site, the Page is rendered, using the shared Layout, stored in `~\Site\Pages\Shared\_Layout.cshtml`. This Layout defines which [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS) references added to the `<head>` HTML element, on every page as references to styles and defines the `JavaScript` initialization that needs to take place once the Page is fully loaded on the Browser.

For Barcode Scanning support, there are additional [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS) and `JavaScript` initialization that needs to take place.


 The following is the updated `_Layout.cshtml` (changes added to the `_Layout.cshtml` created with template's current version at the time this documentation was written).

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0" />
    <meta name="google" content="notranslate" />
    <title>@ViewData["Title"] - ExpoSite</title>

    <link rel="stylesheet" href="~/lib/asna-expo/css/expo.css" />
    <link rel="stylesheet" href="~/lib/asna-expo/css/barcodes.css" />
    <link rel="stylesheet" href="~/css/site.css" />
</head>
<body>
    @RenderBody()

    <script type="module">
        import { Barcodes } from '../lib/asna-expo/js/barcode-detection/barcode-field.js';
        import { Page } from '../lib/asna-expo/js/asna.js';

        Barcodes.init({ formId: 'MonarchForm' });
        Page.init({ formId: 'MonarchForm' });
    </script>

    @RenderSection("Scripts", required: false)
</body>
</html>
```

The changes are:

1. New reference added to the `<head>` linking to stylestheet `barcode.css`.
2. New module `import` from `barcode-detection/barcode-field.js` (which itself references the rest of [ZXing](https://github.com/zxing-js) ).
3. Now that `Barcodes` symbol has been imported, the call to the function `Barcodes.init()` function is added (to run after the Page has fully loaded into the Browser).

## libman.json additions.

Thw following is the updated `~\Site\libman.json` (changes added to the `libman.json` created with template's current version at the time this documentation was written).

```json
{
  "version": "1.0",
  "libraries": [
    {
      "provider": "jsdelivr",
      "library": "asnaqsys/asna-qsys-expo-web-content@5.0.1",
      "destination": "wwwroot/lib/asna-expo",
      "files": [
        "**/*",
        "!.github/**/*",
        "!css/*.min.*",
        "!js/*.min.*",
        "!js/**/*.min.*"
      ]
    },
    {
      "provider": "jsdelivr",
      "library": "asnaqsys/asna-qsys-expo-barcodes@2.0.2",
      "destination": "wwwroot/lib/asna-expo",
      "files": [
        "**/*",
        "!.github/**/*",
        "!css/*.min.*",
        "!js/*.min.*",
        "!js/**/*.min.*",
        "!js/*.md"
      ]
    }
  ]
}
```

Notice the new library added to the `"libraries"` array, that will download the `asna-qsys-expo-barcodes` `JavaScript` and `CSS` files from the [jsondelivr CDN](https://www.jsdelivr.com/package/gh/asnaqsys/asna-qsys-expo-barcodes?tab=files).



## Example of Page using DdsBarcodeField

The following is a Basic Page, with one record format `HOMEMENU` including an input field `PRCODE` that is intended to receive the value of a code scanned from a Barcode.

```html
@page
@model HELLODSPF
@{
    ViewData["Title"] = "HELLODSPF";
    int pageTabIndex = 1;
}

<form id="MonarchForm" method="post">
    <DdsFile DisplayPageModel="Model" KeyNames="F3 'EXIT';" >

        <DdsFunctionKeys Location=HorizontalBottom />

        <main role="main" class="display-element-uninitialized">
            <DdsRecord For="HOMEMENU">
                <div Row="1">
                    <DdsConstant Col="2" Text=@System.Environment.UserName />
                    <DdsConstant Col="29" Text="BARCODE DETECTION TEST" Color="DarkBlue" />
                    <DdsConstant Col="64" Text=@DateTime.Today.ToString(@"MM\/dd\/yy") />
                    <DdsConstant Col="73" Text=@DateTime.Now.ToString("HH:mm:ss") />
                </div>
                <div Row="3">
                    <DdsConstant Col="2" Text="CODE:" />
                    <DdsBarcodeField Col="7" For="HOMEMENU.PRCODE" 
                    ScanningTimeoutSeconds=0
                    VirtualRowCol="3,16" PositionCursor="*True" tabIndex=@pageTabIndex++ />
                </div>
            </DdsRecord> @* HOMEMENU *@

            <DdsMessagePanel class="dds-message-panel"/>

        </main>
    </DdsFile>
</form>
```