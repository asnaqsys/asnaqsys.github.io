---
title: "DdsBarcodeFieldTagHelper class"
description: "Defines a character input element (code) that may be read from a video source, by scanning images on each frame, identifying patterns according to Bar"
last_modified_at: 2024-08-09T16:19:09Z
---

Defines a character input element (code) that may be read from a video source, by scanning images on each frame, identifying patterns according to Barcode or QR Code pictorial representation.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html) --> [DdsCharFieldTagHelper](/reference/expo/qsys-expo-tags/dds-char-field-tag-helper.html)
<br>
<br>

## Remarks

The Barcode scanning feature requires at least one video device accesible to the Web Browser. Typically the video device is the main Mobile Phone camera (with auto-focus).

The Browser requires the appropriate permissions to access the Camera.

Modern Mobile Phones may have more than one camera. The DdsBarcodeFieldTag looks for one with a title including one of these words: `Back` or `back`. If no camera identifies itself with a title containing one of these words, the first camera listed (with video capabilities) is selected by default.

A video-preview window is presented (below the DdsBarcodeFieldTag instance - pushing momentarily the page down), with a collection of small buttons to the right of the window labeld "1", "2", "3", etc. These buttons represent the first, second, third, etc. cameras. Tapping (or clicking) any of the buttons will activate that camera.

There is a button labeled "x" available to **Cancel** the scanning process prematurely.

As soon as the code in the Barcode is identified:

1. An audible alarm sounds to notify that the Barcode has been succesfuly read.
2. The value (code) read is pasted into the value of the DdsBarcodeFieldTag input instance. 
3. The Video preview (with the available options as buttons) is removed from the Page.

Normally the Application will expect only one or two Barcode formats to be used. The barcode detection performance can be improved if the Barcode format(s) is enabled by setting the appropriate `Hint` value to `true` (for any of the listed properties below).

>Note: [Some browsers restrict the use of the camera for secure connections](https://www.digicert.com/blog/https-only-features-in-browsers). Beware that `http` protocol may **NOT** work for Barcode scanning. The development use of *Self-signed* certificate may require additional user consent to display pages on your site.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_Aztec_2D | Aztec 2D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_CODABAR_1D | CODABAR 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_Code_128_1D | Code 128 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_Code_39_1D | Code 39 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_Code_93_1D | Code 93 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_Data_Matrix_2D | Data Matrix 2D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_EAN_13_1D | EAN-13 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_EAN_8_1D | EAN-8 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_ITF_1D | ITF 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_MaxiCode_2D | MaxiCode 2D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_PDF417 | PDF417 Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_QR_Code_2D | QR Code 2D likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_RSS_14 | RSS_14 Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_RSS_EXPANDED | RSS EXPANDED Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_UPC_A_1D | UPC-A 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_UPC_E_1D | UPC-E 1D Barcode likely used to be used to represent the value for this field. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Hint_UPC_EAN_Extension | UPC/EAN Extension Barcode likely used to be used to represent the value for this field. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ScanningTimeoutSeconds | Timeout in seconds for the barcode to be identified. If no detection succeeds within the timeout (since the scan started), the Preview User Interface is removed (canceling the scan). Set to zero to make it indefinite. |
