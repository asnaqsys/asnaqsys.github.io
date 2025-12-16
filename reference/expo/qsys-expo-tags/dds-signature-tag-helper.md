---
title: "DdsSignatureTagHelper class   | QSYS API Reference Guide"
description: "Defines an element where a signature can be captured "
last_modified_at: 2024-08-09T17:26:17Z
---

Defines an element where a signature can be captured

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0) --> [FieldBase](/reference/expo/qsys-expo-tags/field-base.html) --> [DdsFieldBase](/reference/expo/qsys-expo-tags/dds-field-base.html)
<br>
<br>

## Remarks

`DdsSignature` Tag Helper provides a Display element that shows a depiction of a hand written [signature](https://en.wikipedia.org/wiki/Signature).
When bound to an input-capable field in the Model, it allows to capture the [signature](https://en.wikipedia.org/wiki/Signature) by recording a series of line and curve sketches using an input device (such as mouse, or finger movements on a touch device).

The `DdsSignature` Tag Helper can be configured to add a date stamp (in the form of a watermark), to set a reference for the signature creation.

The field bound to the Model is a [FixedString](/concepts/program-structure/qsys-fixedtypes.html#asnaqsysfixedstring) that holds the depiction of the signature as an [Base64-encoded](https://en.wikipedia.org/wiki/Base64) [SVG](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics) image. SVG images provide a compact lossless image format that can be converted to any other [Raster image](https://en.wikipedia.org/wiki/Raster_graphics) format (png, jpeg, etc.)

When the sketches of the signature being captured should exceeds the length of the field bound to it, the `DdsSignature` Tag Helper will `simplify` the [SVG](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics) (lowering its quality) to make it fit into the allocated length.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AspectRatio | Gets or sets the aspect-ratio of the image used to paint or capture the signature. Format is width:height (in dimension proportion units). Defaults to 3:1 |
| [CharAttribute](/reference/expo/qsys-expo-model/char-attribute.html) | CharAttribute | Gets the CharAttribute attribute from the Model |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | DateStampWhenSigning | Gets or sets value indicating if the date should be stamped at the time the signature was captured |
| [FieldAttribute](/reference/expo/qsys-expo-model/field-attribute.html) | FieldAttribute | Gets the FieldAttribute from the Model |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | InvalidEmptySignatureErrorText | Gets or sets value indicating that the user did not draw enough strokes to make a valid signature |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PenDownOutsideSignatureWarningText | Gets or sets value indicating that the user is tracing strokes outside the capture area of the box |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SignatureIsTooElaborateWarningText | Gets or sets a value that displays as a warning when the image is too commplex to be stored in an encoded string (exceeds max. field length) |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SignEditorCancelButtonText | Gets or sets the stroke editor's Cancel button text |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SignEditorDoneButtonText | Gets or sets the stroke editor's Done button text |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SignEditorEraseButtonText | Gets or sets the stroke editor's Erase button text |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SignEditorTitleText | Gets or sets the stroke editor's Title text  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SignLinkText | Gets or sets the value of the label used as a link to the image stroke editor |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | ValueFieldLength | Gets or sets value defining the maximum length of the field which holds the image encoded   |

## Page Example

The following field specification on a Page defines a field named `SIGNATURE` on a class derived from `DisplayPageModel`, for record format `RECORD`.

> Note: When capturing strokes for a handwritten signature, ensure the field length can accommodate the SVG vector data stored as a string. Keep in mind that [Base64-encoding increases size by roughly 33%](https://en.wikipedia.org/wiki/Base64).

```html
<div Row="18">
    <DdsConstant Col="2" Text="Signature:" />
    <DdsSignature Col="15" ColSpan="60"
        For="RECORD.SIGNATURE" 
        SignLinkText="Sign Here!" 
        SignEditorTitleText="Use mouse or finger to sign"
        DateStampWhenSigning=true 
        />
</div>
```

A constant labeled `Signature:` appears on row 18, column 2. The `DdsSignature` tag helper appears on the same row at column 15, with a width of 60 characters.

The `DisplayPageModel` model code would look like:

```cs
        [
            Record(EraseFormats = "*ALL")
        ]
        public class RECORD_Model : RecordModel
        {
            .
            .
            .

            [Char(8192)]
            public string SIGNATURE { get; set; }
```

