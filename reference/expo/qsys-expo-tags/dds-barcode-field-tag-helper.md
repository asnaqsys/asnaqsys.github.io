---
title: "DdsBarcodeFieldTagHelper class"
description: "Defines a character input element (code) that may be read from a video source, by scanning images on each frame, identifying patterns according to Bar"
last_modified_at: 2024-09-26T21:21:26Z
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

>Important: `DdsBarcodeFieldTag` requires additional site configuration to work properly. Please read [Expo Client-Side Barcode Scanning Support](/manuals/configuration/expo-client-side-barcode-scan-config.html) on the Manuals / Configuration section.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | AidKey | Attention or Function key to be posted when Barcode is detected (as if the user had pressed that keyboard key). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HintAllowEAN_Extensions | Comma separated list of lengths, listing the allowed extension lengths for EAN or UPC Barcodes. For example "2, 5". If it is optional to have an extension, do not set this hint. If this is set, and a UPC or EAN Barcode is found but an extension is not, then no result will be returned at all. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HintAllowedITF_Lengths | When Barcode format ITF is detected, only the valid lengths of encoded data in this comma separated list of lengths is considered valid. If not set, it is assumed the valid ITF lengths are:  6, 8, 10, 12, 14. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintAssumeCode39CheckDigit | When Barcode format CODE_39 is detected and this property is true, treat the last data character as a check digit, not data, and verify that the checksum passes. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintAssumeGS1_CODE_128 | Assume the Barcode is being processed as a GS1 Barcode, and modify behavior as needed. Affects FNC1 handling for CODE 128 (aka GS1-128) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HintCharacterSet | Specifies what character encoding to use where applicable ("SJIS", "GB2312", "ISO8859_1", "EUC_JP" or "UTF8" ). Defaults to "UTF8" |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintEnableCODE39_ExtendedMode | Enable CODE 39 Extended Mode. When enabled, Code 39 reader will attempt to decode extended sequences in the text. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatAZTEC | Aztec 2D Barcode format likely used to be used to represent the value for this field. (Use "AZTEC" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatCODABAR | CODABAR 1D Barcode format likely used to be used to represent the value for this field. (Use "CODABAR" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatCODE_128 | Code 128 1D Barcode format likely used to be used to represent the value for this field. (Use "CODE_128" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatCODE_39 | Code 39 1D Barcode format likely used to be used to represent the value for this field. (Use "CODE_39" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatCODE_93 | Code 93 1D Barcode format likely used to be used to represent the value for this field. (Use "CODE_93" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatDATA_MATRIX | Data Matrix 2D Barcode format likely used to be used to represent the value for this field. (Use "DATA_MATRIX" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatEAN_13 | EAN-13 1D Barcode format likely used to be used to represent the value for this field. (Use "EAN_13" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatEAN_8 | EAN-8 1D Barcode format likely used to be used to represent the value for this field. (Use "EAN_8" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatITF | ITF 1D Barcode format likely used to be used to represent the value for this field. (Use "ITF" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatMAXICODE | MaxiCode 2D Barcode format likely used to be used to represent the value for this field. (Use "MAXICODE" if using HintFormatOrderedList property). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | HintFormatOrderedList | For advanced Hint Format configuration, enter on this property a list of string names indicating the possible formats the Barcode reader may encounter.The order in the list may optimize the scanning performance. List first the most likely format identifiers to be encountered.For the name of the identifiers see the help on each of the boolean HintFormatXXXX properties. Use blanks, commas or semi-colons to separate each format identifier name. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatPDF_417 | PDF417 Barcode format likely used to be used to represent the value for this field. (Use "PDF_417" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatQR_CODE | QR Code 2D format likely used to be used to represent the value for this field. (Use "QR_CODE" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatRSS_14 | RSS_14 Barcode format likely used to be used to represent the value for this field. (Use "RSS_14" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatRSS_EXPANDED | RSS EXPANDED Barcode format likely used to be used to represent the value for this field. (Use "RSS_EXPANDED" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatUPC_A | UPC-A 1D Barcode format likely used to be used to represent the value for this field. (Use "UPC_A" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatUPC_E | UPC-E 1D Barcode format likely used to be used to represent the value for this field. (Use "UPC_E" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintFormatUPC_EAN_EXTENSION | UPC/EAN Extension Barcode format likely used to be used to represent the value for this field. (Use "UPC_EAN_EXTENSION" if using HintFormatOrderedList property). |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintPureBarcode | Barcodes are "pure" meaning, monochrome images which contains only an unrotated, unskewed, image of a code, with some white border around it.Enabling this hint (when applicable) optimizes detection performance significantly.  |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | HintTryHarder | Spend more time to try to find a Barcode; optimize for accuracy, not speed. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ScanningTimeoutSeconds | Timeout in seconds for the Barcode to be identified. If no detection succeeds within the timeout (since the scan started), the Preview User Interface is removed (canceling the scan). Set to zero to make it indefinite. |
