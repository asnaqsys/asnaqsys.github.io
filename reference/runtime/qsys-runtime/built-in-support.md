---
title: "BuiltInSupport class          | QSYS API Reference Guide"
description: "Contains static methods to perform certain RPG Built In functions. "
last_modified_at: 2024-08-09T16:18:25Z
---

Contains static methods to perform certain RPG Built In functions.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MaxDecimals | Maximum Decimals supported. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | MaxIntegrals | Maximum Integrals supported. |

## Methods

| Signature | Description |
| --- | --- |
| [BitOff](#byte-bitoffstring-mask-byte-b)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Allows bits to be set off in the input b parameter based upon a mask specified in the mask parameter.
| [BitOn](#byte-bitonstring-mask-byte-b)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte)) | Allows bits to be set on in the Target parameter based upon a mask specified in the Mask parameter.
| [CompareStrings](#int-comparestringsstring-sa-string-sb)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Compares two specified string objects using RPG semantics and returns an integer that indicates their relative position in the sort order.If necessary, one of the strings is padded with blanks to make both strings the same length.
| [ConvertDoubleToString](#string-convertdoubletostringdouble-d-bool-isfloat)([Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %EDITFLT: Convert a floating point number to IBMi's string representation.
| [DoBuiltInCharDec](#decimal-dobuiltinchardecstring-charfld-int-integrals-int-decimals-bool-halfadjust)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %DEC/%DECH(character). Converts a character string to a decimal numeric value, with the given length and decimal positions.
| [DoBuiltInCheck](#int-dobuiltincheckstring-cmpstr-string-basestring-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECK. Finds in baseStr the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position.
| [DoBuiltInCheckR](#int-dobuiltincheckrstring-cmpstr-string-basestring-int-startpos-bool-isdefaultstartpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %CHECKR. Finds in baseStr the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position, starting at the end of baseStr.
| [DoBuiltInDigitReplace](#string-dobuiltindigitreplaceint-length-int-startpos-decimal-repdigits-string-basestring)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Replace part of a string with the digits in a decimal number.
| [DoBuiltInDigitSubSt](#decimal-dobuiltindigitsubststring-basestring-int-startpos-int-sublen)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Get a substring representing a decimal number and return the decimal number according to the Culture formatting.
| [DoBuiltInLookup](#int-dobuiltinlookupobject-source-array-array-int-startpos-int-celements)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %LOOKUP: Searches an array for the specified element value.
| [DoBuiltInLookupXX](#int-dobuiltinlookupxxobject-source-array-array-int-startpos-int-celements-bool-searchhi-bool-searchlo-bool-searcheq)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %LOOKUPXX: Searches an array for the specified element value.
| [DoBuiltInReplace](#string-dobuiltinreplaceint-length-int-startpos-string-repstring-string-basestring)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Replaces characters in a string with a given replacement string.
| [DoBuiltInScan](#int-dobuiltinscanstring-cmpstr-string-basestring-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %SCAN: Find a string within another and return the 1-based starting position where the match starts.
| [DoBuiltInSubSt](#string-dobuiltinsubststring-basestring-int-startpos-int-sublen)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %SUBST: Get a substring.
| [DoBuiltInSubStAssign](#string-dobuiltinsubstassignstring-basestring-int-startpos-int-sublen-string-replacestr-bool-isrightadjust)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %SUBST: Set a substring.
| [DoBuiltInTLookup](#bool-dobuiltintlookupobject-source-array-array-int32-tableindex-int32-alttableindex)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %TLOOKUP: Searches an array representing a RPG table for the specified element value.
| [DoBuiltInTLookupXX](#bool-dobuiltintlookupxxobject-source-array-array-int32-tableindex-int32-alttableindex-bool-searchhi-bool-searchlo-bool-searcheq)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %TLOOKUPXX: Searches an array representing a RPG table for the specified element value.
| [DoCheck](#void-docheckstring-cmpstr-string-basestring-bool-isdefaultstartpos-int-startpos-int32-result)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECK. Finds in baseString the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position.
| [DoCheckArrayResult](#void-docheckarrayresultstring-cmpstr-string-basestring-bool-isdefaultstartpos-int-startpos-array-nomatcharray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | RPG's %CHECK. Finds in baseString all the occurrences that are different from any of the characters in cmpStr and returns their 1-based position in an array.
| [DoCheckR](#void-docheckrstring-cmpstr-string-basestring-bool-isdefaultstartpos-int-startpos-int32-result)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's %CHECKR. Finds in baseStr the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position, starting at the end of baseStr.
| [DoCheckRArrayResult](#void-docheckrarrayresultstring-cmpstr-string-basestring-bool-isdefaultstartpos-int-startpos-array-nomatcharray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | RPG's %CHECKR. Finds in baseString all the occurrences that are different from any of the characters in cmpStr and returns their 1-based position in an array, starting at the end of baseStr..
| [DoConcat](#string-doconcatstring-prefix-string-suffix-int-blanks)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Concatenate two strings, adjusting the number of blanks at the end of prefix to the given number.
| [DoIntDecimal](#int-dointdecimaldecimal-thedecimal-bool-ishalfadjust)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %INT/%INTH for a decimal argument. Convert a decimal number to an integer.
| [DoIntDouble](#int-dointdoubledouble-thedouble-bool-ishalfadjust)([Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %INT/%INTH for a double (8-byte floating point number) argument. Convert a double number to an integer.
| [DoIntString](#int-dointstringstring-thestring-bool-ishalfadjust)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %INT/%INTH for a string. Convert a string representing a number in any of the supported RPG formats to an integer.
| [DoScan](#int-doscanstring-cmpstr-string-basestr-int-cmplen-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Scans a string (baseStr) for a substring (cmpStr).
| [DoScanArrayResult](#void-doscanarrayresultstring-cmpstr-string-basestr-int-cmplen-int-startpos-array-fndposarray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | Scans a string (baseStr) for all occurrences of a substring (cmpStr). The starting positions of the occurrences found are saved in the fndPosArray array parameter.
| [DoSubStr](#string-dosubstrstring-basestr-int-sublen-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Extracts a substring out of a given string.
| [DoUnsDecimal](#int-dounsdecimaldecimal-thedecimal-bool-ishalfadjust)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %UNS/%UNSH for a decimal argument. Convert a decimal number to an unsigned (positive) integer.
| [DoUnsDouble](#int-dounsdoubledouble-thedouble-bool-ishalfadjust)([Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %UNS/%UNSH for a double (8-byte floating point number) argument. Convert a double number to an unsigned (positive) integer.
| [DoUnsString](#int-dounsstringstring-thestring-bool-ishalfadjust)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | RPG's %UNS/%UNSH for a string. Convert a string representing a number in any of the supported RPG formats to an unsigned (positive) integer.
| [DoXlate](#string-doxlatestring-mapfrom-string-mapto-string-basestr-int-startpos)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos.
| [GetBinaryAsChars](#void-getbinaryascharsdecimal-number-char--chararray-int-offset-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal number to its representation as a Binary decimal in a character array.
| [GetBinaryFromChars](#decimal-getbinaryfromcharschar--chararray-int-offset-int-digits-int-decimals)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert an array of characters representing a Binary decimal number to decimal.
| [GetDate](#datetime-getdatechar--chararray-int-offset-string-formatstring)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get the DateTime value represented by a fixed date/time value stored in a char array.
| [GetDateArrayInCharArray](#void-getdatearrayinchararrayarray-array-char--target-int-targetindex-string-formatstring)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Copy an array of DateTime values onto a character array of fixed date/time values in the given format.
| [GetDateInCharArray](#void-getdateinchararraydatetime-date-char--chararray-int-offset-string-formatstring)([DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get the fixed date/time representation of a DateTime value, store the result in a character array.
| [GetDecimalArrayInCharArray](#void-getdecimalarrayinchararrayarray-decimalarray-char--target-int-targetindex-int-cintegrals-int-cdecimals)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Copy an array of decimal values onto a character array of zoned decimal numbers.
| [GetDecimalFromZoned](#decimal-getdecimalfromzonedchar--chararray-int-offset-int-cintegralsavail-int-cdecimalsavail)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Get the decimal number represented by a zoned decimal value stored in a char array.
| [GetPackedAsChars](#void-getpackedascharsdecimal-number-char--chararray-int-offset-int-digits)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal number to Packed representation.
| [GetPackedFromChars](#decimal-getpackedfromcharschar--chararray-int-offset-int-length-int-decimals)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert an array of characters representing a Packed decimal number to decimal.
| [GetZoned](#void-getzoneddecimal-decnum-char--chararray-int-offset-int-cintegralsavail-int-cdecimalsavail)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Get the zoned decimal representation of a decimal number, store the result in a character array.
| [LoadPictureFromFile](#image-loadpicturefromfilestring-filename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Loads an image file.
| [MapFromBinary](#string-mapfrombinarydecimal-number-int-digits-int-decimals)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a decimal number to its string representation as a Binary decimal.
| [MapToBinary](#decimal-maptobinarystring-basestring-int-digits-int-decimals)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Convert a string representing a Binary decimal number to decimal.
| [MoveArrayElemToElem](#void-movearrayelemtoelemarray-source-array-target-int-isourcestart-int-itargetstart-bool-pad-bool-targetisfixeddecimal-int-targetintegrals-int-targetdecimals-bool-sourceisfixeddecimal-int-sourcedecimals-bool-targetisdatetime-string-targetdateformat-bool-sourceisdatetime-string-sourcedateformat)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Move data between arrays of arbitrary RPG types represented with system types.
| [MoveArrayFromArray](#void-movearrayfromarrayarray-source-array-target-int-sourcestartat-int-targetstartat-bool-pad)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Moves data from one array to another, where the array elements are of the same size.
| [MoveArrayToString](#string-movearraytostringboolean-boz-array-source-string-target-int-sourcestartat-bool-pad)([Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Serialize an array onto a target string.
| [MoveComplexArray](#void-movecomplexarrayarray-source-array-target-int-sourcestartat-int-targetstartat-bool-pad)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Moves data from one array to another, where the array elements are of different size.
| [MoveFigurativeToElem](#void-movefigurativetoelemarray-target-int-itargetstart-object-obj)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Fill a given array with the specified object.
| [MoveStringToArray](#void-movestringtoarraystring-source-array-target-int-targetstartat-bool-pad)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Deserialize a string onto a character-typed array.
| [OsExec](#void-osexecstring-commandline-int-windowstyle-string-operationstring-string-directory-bool-wait-int32-returncode)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | The OSEXEC command opens or prints a specified file.  The file can be an executable file or a file that is associated with a program.
| [OsExecWithExitCode](#void-osexecwithexitcodestring-commandline-int-windowstyle-string-operationstring-string-directory-bool-wait-int32-returncode-int32-exitcode)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | The OSEXEC command opens or prints a specified file.  The file can be an executable file or a file that is associated with a program.
| [SetArrayDates](#void-setarraydatesarray-array-char--source-int-sourceindex-string-formatstring)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Deserialize an array of fixed date/time values stored in a character array onto a DateTime array.
| [SetArrayDecimals](#void-setarraydecimalsarray-array-char--source-int-sourceindex-int-cintegrals-int-cdecimals)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Deserialize an array of zoned decimals stored in a character array onto a decimal array.
| [SetPosNegBoz](#void-setposnegbozstring-test-boolean-pos-boolean-neg-boolean-boz-bool-testisnumeric)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Sets flags depending on the value of the test argument. The flags indicate a positive, negative, or blank-or-zero test value.
| [SortArr](#void-sortarrarray-arraytosort)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | Sort an array using RPG sorting rules.
| [SortNonContiguosArr](#void-sortnoncontiguosarrarray-basearray-array-arraytosort)([Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0)) | Sort a base array using a second array as a key array, using RPG sorting rules. This method only sorts arrays of strings or arrays of decimal numbers.
| [TestBits](#void-testbitsbyte-b-string-mask-boolean-off-boolean-on-boolean-eq)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Compares the bits in mask with the corresponding bits in b.
| [TestBitsWithByte](#void-testbitswithbytebyte-b-byte-maskbyte-boolean-off-boolean-on-boolean-eq)([Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Compares the bits in maskByte with the corresponding bits in b.
| [ToChar](#char-tocharstring-sa)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the first character of a specified string to a Unicode character.

### byte BitOff([string mask](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Allows bits to be set off in the input b parameter based upon a mask specified in the mask parameter.

```cs
byte BitOff(string mask, byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | Mask can contain: Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036' in Factor 2. A valid character expression. Hexadecimal literal (H'85') for example(Binary 10000101). Named constant up to 8 positions long containing the bit numbers to be set OFF.
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | Input byte value.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | BitOff result as byte.

### byte BitOn([string mask](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte))

Allows bits to be set on in the Target parameter based upon a mask specified in the Mask parameter.

```cs
byte BitOn(string mask, byte b)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | BitOn param mask.
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | Input byte value.

#### Returns

| Type | Description
| --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | BitOn result as byte.

### int CompareStrings([string sA](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string sB](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Compares two specified string objects using RPG semantics and returns an integer that indicates their relative position in the sort order.If necessary, one of the strings is padded with blanks to make both strings the same length.

```cs
int CompareStrings(string sA, string sB)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sA | First string to compare.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sB | Second string to compare.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | A signed integer number that indicates the lexical relationship between the two strings: less than zero meanssA precedes sB in the sort order; zero, the strings are equal; greater than zero, sA follows sB in the sort order.

### string ConvertDoubleToString([double d](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool isFloat](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %EDITFLT: Convert a floating point number to IBMi's string representation.

```cs
string ConvertDoubleToString(double d, bool isFloat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | d | The floating point value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFloat | True is d is a 4-byte float.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The string representation of the floating point number.

### decimal DoBuiltInCharDec([string charFld](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int integrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool halfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %DEC/%DECH(character). Converts a character string to a decimal numeric value, with the given length and decimal positions.

```cs
decimal DoBuiltInCharDec(string charFld, int integrals, int decimals, bool halfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | charFld | The string to convert to decimal numeric.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | integrals | The number of integral digits of the result.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions of the result.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | halfAdjust | True to half-adjust the result to the given number of digits.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The resulting decimal number.

### int DoBuiltInCheck([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %CHECK. Finds in baseStr the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position.

```cs
int DoBuiltInCheck(string cmpStr, string baseString, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The characters to search for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to test.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position where the search should start.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The 1-based position of the found character, or 0 if it was not found.

### int DoBuiltInCheckR([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool isDefaultStartPos](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %CHECKR. Finds in baseStr the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position, starting at the end of baseStr.

```cs
int DoBuiltInCheckR(string cmpStr, string baseString, int startPos, bool isDefaultStartPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The characters to search for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to test.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position where the search should start.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultStartPos | True to start at the end of baseStr.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The 1-based position of the found character, or 0 if it was not found.

### string DoBuiltInDigitReplace([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [decimal repDigits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Replace part of a string with the digits in a decimal number.

```cs
string DoBuiltInDigitReplace(int length, int startPos, decimal repDigits, string baseString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length to replace.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Position where the replacement starts.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | repDigits | The replacement digits to add to the string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The target string.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of baseString with the indicated segment replaced.

### decimal DoBuiltInDigitSubSt([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Get a substring representing a decimal number and return the decimal number according to the Culture formatting.

```cs
decimal DoBuiltInDigitSubSt(string baseString, int startPos, int subLen)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string containing the repesentation of a decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based starting position of the decimal number representation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | Length of the decimal number representation.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number.

### int DoBuiltInLookup([object source](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cElements](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %LOOKUP: Searches an array for the specified element value.

```cs
int DoBuiltInLookup(object source, Array array, int startPos, int cElements)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | source | The element value being searched for in the array.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The array to search.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The array index where the search will begin.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cElements | The number of elements to search.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The position in the array where the element was found, or -1 in not found.

### int DoBuiltInLookupXX([object source](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cElements](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool searchHi](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool searchLo](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool searchEq](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %LOOKUPXX: Searches an array for the specified element value.

```cs
int DoBuiltInLookupXX(object source, Array array, int startPos, int cElements, bool searchHi, bool searchLo, bool searchEq)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | source | The element value being searched for in the array.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The array to search.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The array index where the search will begin.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cElements | The number of elements to search.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | searchHi | True to search for greater than.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | searchLo | True to search for less than.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | searchEq | True to search for equal.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The position in the array where the element was found, or -1 in not found.

### string DoBuiltInReplace([int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string repString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Replaces characters in a string with a given replacement string.

```cs
string DoBuiltInReplace(int length, int startPos, string repString, string baseString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | Length to replace, pass -1 to use the length of the replacement string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | Position where to start the replacement.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | repString | Replacement string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | String to modify.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value.

### int DoBuiltInScan([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %SCAN: Find a string within another and return the 1-based starting position where the match starts.

```cs
int DoBuiltInScan(string cmpStr, string baseString, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The string to find.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to scan.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based starting position where the scan should start.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The 1-based position where the match starts, or 0 if not found.

### string DoBuiltInSubSt([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's %SUBST: Get a substring.

```cs
string DoBuiltInSubSt(string baseString, int startPos, int subLen)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | String to search.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | 1-based starting position of the substring to extract.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | Length of the desired substring. Use -1 to get the substring from startPos to the end.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The substring.

### string DoBuiltInSubStAssign([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string replaceStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isRightAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %SUBST: Set a substring.

```cs
string DoBuiltInSubStAssign(string baseString, int startPos, int subLen, string replaceStr, bool isRightAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | String to search.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | 1-based starting position of the substring to extract.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | Length of the desired substring. Use -1 to get the substring from startPos to the end.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | replaceStr | The string to replace in baseString.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isRightAdjust | If the length of replaceStr is not equal to subLen, indicates whether the replacement should be right adjusted (True), or left  adjusted (False).

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of baseString with the replacement.

### bool DoBuiltInTLookup([object source](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32& tableIndex](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32& altTableIndex](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %TLOOKUP: Searches an array representing a RPG table for the specified element value.

```cs
bool DoBuiltInTLookup(object source, Array array, Int32& tableIndex, Int32& altTableIndex)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | source | The element value being searched for in the table.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The table to search.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | tableIndex | Out value that contains the 1-based index where the element was found, or 0 if not found.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | altTableIndex | Out value that contains the 1-based index where the element was found, or 0 if not found.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the element was found. False otherwise.

### bool DoBuiltInTLookupXX([object source](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Int32& tableIndex](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32& altTableIndex](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [bool searchHi](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool searchLo](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool searchEq](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %TLOOKUPXX: Searches an array representing a RPG table for the specified element value.

```cs
bool DoBuiltInTLookupXX(object source, Array array, Int32& tableIndex, Int32& altTableIndex, bool searchHi, bool searchLo, bool searchEq)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | source | The element value being searched for in the table.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The table to search.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | tableIndex | Out value that contains the 1-based index where the element was found, or 0 if not found.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | altTableIndex | Out value that contains the 1-based index where the element was found, or 0 if not found.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | searchHi | True to search for greater than.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | searchLo | True to search for less than.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | searchEq | True to search for equal.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the element was found. False otherwise.

### void DoCheck([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isDefaultStartPos](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Int32& result](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %CHECK. Finds in baseString the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position.

```cs
void DoCheck(string cmpStr, string baseString, bool isDefaultStartPos, int startPos, Int32& result)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The characters to search for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to test.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultStartPos | True to start at the beginning of baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position where the search should start.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | result | The 1-based position of the found character, or 0 if it was not found.

### void DoCheckArrayResult([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isDefaultStartPos](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Array noMatchArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

RPG's %CHECK. Finds in baseString all the occurrences that are different from any of the characters in cmpStr and returns their 1-based position in an array.

```cs
void DoCheckArrayResult(string cmpStr, string baseString, bool isDefaultStartPos, int startPos, Array noMatchArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The characters to search for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to test.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultStartPos | True to start at the beginning of baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position where the search should start.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | noMatchArray | The 1-based position of the found characters, in order. Any additional positions in the array will be filled with 0.

### void DoCheckR([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isDefaultStartPos](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Int32& result](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

RPG's %CHECKR. Finds in baseStr the first occurrence that is different from any of the characters in cmpStr and returns its 1-based position, starting at the end of baseStr.

```cs
void DoCheckR(string cmpStr, string baseString, bool isDefaultStartPos, int startPos, Int32& result)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The characters to search for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to test.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultStartPos | True to start at the end of baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position where the search should start.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | result | The 1-based position of the found character, or 0 if it was not found.

### void DoCheckRArrayResult([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isDefaultStartPos](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Array noMatchArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

RPG's %CHECKR. Finds in baseString all the occurrences that are different from any of the characters in cmpStr and returns their 1-based position in an array, starting at the end of baseStr..

```cs
void DoCheckRArrayResult(string cmpStr, string baseString, bool isDefaultStartPos, int startPos, Array noMatchArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | The characters to search for.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The string to test.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultStartPos | True to start at the end of baseString.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based position where the search should start.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | noMatchArray | The 1-based position of the found characters, in order. Any additional positions in the array will be filled with 0.

### string DoConcat([string prefix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string suffix](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int blanks](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Concatenate two strings, adjusting the number of blanks at the end of prefix to the given number.

```cs
string DoConcat(string prefix, string suffix, int blanks)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | prefix | The first string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | suffix | The second string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | blanks | The number of blanks to set at the end of prefix. A negative number will leave prefix as it is, without adjusting the blanks at the end.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The concatenation of the modified prefix and suffix.

### int DoIntDecimal([decimal theDecimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool isHalfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %INT/%INTH for a decimal argument. Convert a decimal number to an integer.

```cs
int DoIntDecimal(decimal theDecimal, bool isHalfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | theDecimal | The decimal number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isHalfAdjust | True for half adjust.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The integer conversion of theDecimal, half-adjusted if necessary. 

### int DoIntDouble([double theDouble](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool isHalfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %INT/%INTH for a double (8-byte floating point number) argument. Convert a double number to an integer.

```cs
int DoIntDouble(double theDouble, bool isHalfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | theDouble | The double number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isHalfAdjust | True for half adjust.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The integer conversion of theDouble, half-adjusted if necessary. 

### int DoIntString([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isHalfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %INT/%INTH for a string. Convert a string representing a number in any of the supported RPG formats to an integer.

```cs
int DoIntString(string theString, bool isHalfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isHalfAdjust | True for half adjust.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The integer conversion of theString, half-adjusted if necessary.

### int DoScan([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int cmpLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Scans a string (baseStr) for a substring (cmpStr).

```cs
int DoScan(string cmpStr, string baseStr, int cmpLen, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | Substring to find in the baseStr string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseStr | String to scan.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Length of the substring. Use 0 to use the current length of the substring
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | 1-based position where to start scanning in baseStr.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The 1-based starting position of the substring, if found, or 0 if not found.

### void DoScanArrayResult([string cmpStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int cmpLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Array fndPosArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

Scans a string (baseStr) for all occurrences of a substring (cmpStr). The starting positions of the occurrences found are saved in the fndPosArray array parameter.

```cs
void DoScanArrayResult(string cmpStr, string baseStr, int cmpLen, int startPos, Array fndPosArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmpStr | Substring to find in the baseStr string.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseStr | String to scan.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cmpLen | Length of the substring. Use 0 to use the current length of the substring
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | 1-based position where to start scanning in baseStr.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | fndPosArray | The array where starting positions are saved, in order.

### string DoSubStr([string baseStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int subLen](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Extracts a substring out of a given string.

```cs
string DoSubStr(string baseStr, int subLen, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseStr | The string from where to extract a substring.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | subLen | The length of the desired substring.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based starting position in the baseStr string where the substring starts.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The substring.

### int DoUnsDecimal([decimal theDecimal](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool isHalfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %UNS/%UNSH for a decimal argument. Convert a decimal number to an unsigned (positive) integer.

```cs
int DoUnsDecimal(decimal theDecimal, bool isHalfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | theDecimal | The decimal number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isHalfAdjust | True for half adjust.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The positive integer conversion of theDecimal, half-adjusted if necessary. 

### int DoUnsDouble([double theDouble](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [bool isHalfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %UNS/%UNSH for a double (8-byte floating point number) argument. Convert a double number to an unsigned (positive) integer.

```cs
int DoUnsDouble(double theDouble, bool isHalfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Double](https://learn.microsoft.com/en-us/dotnet/api/system.double?view=net-8.0) | theDouble | The double number.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isHalfAdjust | True for half adjust.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The positive integer conversion of theDouble, half-adjusted if necessary. 

### int DoUnsString([string theString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool isHalfAdjust](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

RPG's %UNS/%UNSH for a string. Convert a string representing a number in any of the supported RPG formats to an unsigned (positive) integer.

```cs
int DoUnsString(string theString, bool isHalfAdjust)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | theString | The string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isHalfAdjust | True for half adjust.

#### Returns

| Type | Description
| --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | The positive integer conversion of theString, half-adjusted if necessary.

### string DoXlate([string mapFrom](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string mapTo](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string baseStr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int startPos](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

RPG's XLATE. Translates characters in the baseString according to MapFrom, MapTo, startPos.

```cs
string DoXlate(string mapFrom, string mapTo, string baseStr, int startPos)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapFrom | From string, if characters are duplicated the first occurrence is used.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mapTo | To string, describes what the characters in mapFrom will become.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseStr | A character expression that contains the string Xlate will operate on.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | startPos | The 1-based start position for baseString.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The resulting string value.

### void GetBinaryAsChars([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal number to its representation as a Binary decimal in a character array.

```cs
void GetBinaryAsChars(decimal number, Char[] charArray, int offset, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | The number to convert.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The array to contain the binary decimal.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The index of the array where the binary decimal will start.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

### decimal GetBinaryFromChars([Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert an array of characters representing a Binary decimal number to decimal.

```cs
decimal GetBinaryFromChars(Char[] charArray, int offset, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The binary decimal number as an array of characters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The index of the character in the array where the binary decimal starts.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number.

### DateTime GetDate([Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string formatString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get the DateTime value represented by a fixed date/time value stored in a char array.

```cs
DateTime GetDate(Char[] charArray, int offset, string formatString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The array containing the fixed date/time value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The index of the first array element where the fixed date/time value starts.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatString | The format encoding the fixed date/time value.

#### Returns

| Type | Description
| --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | The DateTime value equivalent to the fixed date/time in the array.

### void GetDateArrayInCharArray([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] target](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int targetIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string formatString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Copy an array of DateTime values onto a character array of fixed date/time values in the given format.

```cs
void GetDateArrayInCharArray(Array array, Char[] target, int targetIndex, string formatString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The DateTime array source of the operation.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | target | The character array that will receive the date/time values.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetIndex | The index of the element in target where the copy starts.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatString | The format in which the fixed date/time values are stored.

### void GetDateInCharArray([DateTime date](https://docs.microsoft.com/en-us/dotnet/api/system.datetime), [Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string formatString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get the fixed date/time representation of a DateTime value, store the result in a character array.

```cs
void GetDateInCharArray(DateTime date, Char[] charArray, int offset, string formatString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | date | The DateTime value to convert.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The array to store the result.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The index of the first array element where the zoned number starts.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatString | The desired format of the resulting fixed date/time value.

### void GetDecimalArrayInCharArray([Array decimalArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] target](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int targetIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cIntegrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Copy an array of decimal values onto a character array of zoned decimal numbers.

```cs
void GetDecimalArrayInCharArray(Array decimalArray, Char[] target, int targetIndex, int cIntegrals, int cDecimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | decimalArray | The decimal array source of the operation.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | target | The character array that will receive the date/time values.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetIndex | The index of the element in target where the copy starts.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cIntegrals | The number of integral digits in the zoned numbers.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cDecimals | The number of decimal positions in the zoned numbers.

### decimal GetDecimalFromZoned([Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cIntegralsAvail](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cDecimalsAvail](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Get the decimal number represented by a zoned decimal value stored in a char array.

```cs
decimal GetDecimalFromZoned(Char[] charArray, int offset, int cIntegralsAvail, int cDecimalsAvail)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The array containing the zoned decimal value.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The index of the first array element where the zoned number starts.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cIntegralsAvail | Integral positions of the zoned number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cDecimalsAvail | Decimal positions of the zoned number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number corresponding to the zoned decimal representation in the array.

### void GetPackedAsChars([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal number to Packed representation.

```cs
void GetPackedAsChars(decimal number, Char[] charArray, int offset, int digits)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | The number to convert.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The array to hold the packed representation of the number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | Where in the array to start loading the packed representation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The total number of digits of the desired packed number.

### decimal GetPackedFromChars([Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert an array of characters representing a Packed decimal number to decimal.

```cs
decimal GetPackedFromChars(Char[] charArray, int offset, int length, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The input array of characters.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The position in the array where the packed number starts.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number.

### void GetZoned([decimal decNum](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Char\[\] charArray](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int offset](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cIntegralsAvail](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cDecimalsAvail](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Get the zoned decimal representation of a decimal number, store the result in a character array.

```cs
void GetZoned(decimal decNum, Char[] charArray, int offset, int cIntegralsAvail, int cDecimalsAvail)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | decNum | The number to convert.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | charArray | The array to store the result.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | offset | The index of the first array element where the zoned number starts.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cIntegralsAvail | Integral positions of the zoned number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cDecimalsAvail | Decimal positions of the zoned number.

### Image LoadPictureFromFile([string fileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Loads an image file.

```cs
Image LoadPictureFromFile(string fileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fileName | Image file pathname.

#### Returns

| Type | Description
| --- | ---
| [Image](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.image?view=dotnet-plat-ext-8.0) | Image class instance.

### string MapFromBinary([decimal number](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a decimal number to its string representation as a Binary decimal.

```cs
string MapFromBinary(decimal number, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | number | The number to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The binary decimal representation as a string.

### decimal MapToBinary([string baseString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int digits](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Convert a string representing a Binary decimal number to decimal.

```cs
decimal MapToBinary(string baseString, int digits, int decimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | baseString | The binary decimal number as a string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | digits | The number of digits in the decimal number.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | The number of decimal positions in the decimal number.

#### Returns

| Type | Description
| --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | The decimal number.

### void MoveArrayElemToElem([Array source](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int iSourceStart](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int iTargetStart](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool targetIsFixedDecimal](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int targetIntegrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool sourceIsFixedDecimal](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int sourceDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool targetIsDateTime](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [string targetDateFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool sourceIsDateTime](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [string sourceDateFormat](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Move data between arrays of arbitrary RPG types represented with system types.

```cs
void MoveArrayElemToElem(Array source, Array target, int iSourceStart, int iTargetStart, bool pad, bool targetIsFixedDecimal, int targetIntegrals, int targetDecimals, bool sourceIsFixedDecimal, int sourceDecimals, bool targetIsDateTime, string targetDateFormat, bool sourceIsDateTime, string sourceDateFormat)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | source | Source array.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | Target array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iSourceStart | Source array starting index.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iTargetStart | Target array starting index.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True to pad the target array.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | targetIsFixedDecimal | True if the target contains decimal numbers representing fixed-decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetIntegrals | If the target is a fixed decimal number, the integral digits.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetDecimals | If the target is a fixed decimal number, the decimal positions.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | sourceIsFixedDecimal | True if the source contains decimal numbers representing fixed-decimals.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceDecimals | If the source is a fixed decimal number, the decimal positions.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | targetIsDateTime | True if the target is a fixed date/time type.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | targetDateFormat | If the target is a fixed date/time type, the format as a string.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | sourceIsDateTime | True if the source is a fixed date/time type.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sourceDateFormat | If the source is a fixed date/time type, the format as a string.

### void MoveArrayFromArray([Array source](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int sourceStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Moves data from one array to another, where the array elements are of the same size.

```cs
void MoveArrayFromArray(Array source, Array target, int sourceStartAt, int targetStartAt, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | source | Source array.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | Target array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceStartAt | Initial position in source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | Initial position in target.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True if padding with blanks is to be performed when the target array is longer than the data copied from the source.

### string MoveArrayToString([Boolean& boz](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Array source](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [string target](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int sourceStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Serialize an array onto a target string.

```cs
string MoveArrayToString(Boolean& boz, Array source, string target, int sourceStartAt, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | boz | Boolean flag that return true if the resulting string is blanks.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | source | The array to serialize.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | target | The target string.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceStartAt | Index of the array element on where to start serialization.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True to pad the target string with blanks.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The result of serializing the array onto the target string.

### void MoveComplexArray([Array source](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int sourceStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Moves data from one array to another, where the array elements are of different size.

```cs
void MoveComplexArray(Array source, Array target, int sourceStartAt, int targetStartAt, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | source | Source Array.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | Target Array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceStartAt | Initial position in source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | Initial position in target.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True if padding with blanks is to be performed when the target array is longer than the data copied from the source.

### void MoveFigurativeToElem([Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int iTargetStart](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Fill a given array with the specified object.

```cs
void MoveFigurativeToElem(Array target, int iTargetStart, object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | Array to fill.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | iTargetStart | The array element where the copy starts.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | Object to fill array with, must be a compatible type.

### void MoveStringToArray([string source](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Array target](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [int targetStartAt](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool pad](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Deserialize a string onto a character-typed array.

```cs
void MoveStringToArray(string source, Array target, int targetStartAt, bool pad)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The string to deserialize.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | target | The target array.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | targetStartAt | Index of the array element on where to start deserialization.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pad | True to pad the array with blanks.

### void OsExec([string commandLine](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int windowStyle](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string operationString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string directory](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool wait](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32& returnCode](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

The OSEXEC command opens or prints a specified file.  The file can be an executable file or a file that is associated with a program.

```cs
void OsExec(string commandLine, int windowStyle, string operationString, string directory, bool wait, Int32& returnCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | commandLine | Specifies the file to open or print, or the folder to open or explore.  The function can be either an executable file or a document file.  It can also print a document file.  commandLine must contain the complete path of the application to execute.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | windowStyle | The style of the window to open..
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | operationString | Specifies what type of operation is to be performed on the file. The action to take with the file the action processes.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directory | Contains the string that specifies the default directory.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | wait | Determines whether the program will wait for the launched application to end before continuing execution.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returnCode | Reference to the code that indicates success of failure to launch. 0 is sucess, otherwise the error numeric value.

### void OsExecWithExitCode([string commandLine](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int windowStyle](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string operationString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string directory](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool wait](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32& returnCode](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32& exitCode](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

The OSEXEC command opens or prints a specified file.  The file can be an executable file or a file that is associated with a program.

```cs
void OsExecWithExitCode(string commandLine, int windowStyle, string operationString, string directory, bool wait, Int32& returnCode, Int32& exitCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | commandLine | Specifies the file to open or print, or the folder to open or explore.  The function can be either an executable file or a document file.  It can also print a document file.  commandLine must contain the complete path of the application to execute.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | windowStyle | The style of the window to open..
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | operationString | Specifies what type of operation is to be performed on the file. The action to take with the file the action processes.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directory | Contains the string that specifies the default directory.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | wait | Determines whether the program will wait for the launched application to end before continuing execution.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | returnCode | Reference to the code that indicates success of failure to launch. 0 is sucess, otherwise the error numeric value.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | exitCode | Reference to the exit code of the launched application after waiting for it to finish.

### void SetArrayDates([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int sourceIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string formatString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Deserialize an array of fixed date/time values stored in a character array onto a DateTime array.

```cs
void SetArrayDates(Array array, Char[] source, int sourceIndex, string formatString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The target of the operation.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | source | The char array containing fixed date/time values.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceIndex | The index of the first element to extract from source.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatString | The format in which the fixed date/time values are stored.

### void SetArrayDecimals([Array array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Char\[\] source](https://docs.microsoft.com/en-us/dotnet/api/system.char), [int sourceIndex](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cIntegrals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int cDecimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Deserialize an array of zoned decimals stored in a character array onto a decimal array.

```cs
void SetArrayDecimals(Array array, Char[] source, int sourceIndex, int cIntegrals, int cDecimals)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | array | The target of the operation.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | source | The char array containing zoned decimal numbers.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | sourceIndex | The index of the first element to extract from source.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cIntegrals | The number of integral digits in the zoned numbers.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | cDecimals | The number of decimal positions in the zoned numbers.

### void SetPosNegBoz([string test](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Boolean& pos](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& neg](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& boz](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool testIsNumeric](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Sets flags depending on the value of the test argument. The flags indicate a positive, negative, or blank-or-zero test value.

```cs
void SetPosNegBoz(string test, Boolean& pos, Boolean& neg, Boolean& boz, bool testIsNumeric)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | test | The value to test, as a string.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | pos | Positive flag. It will be true if the test parameter represents a positive numeric value.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | neg | Negative flag. It will be true if the test parameter represents a negative numeric value.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | boz | Blank-or-zero flag. It will be true if the test parameter is blanks or represents a numeric value of zero.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | testIsNumeric | Indicates whether the string to test represents a numeric value.

### void SortArr([Array arrayToSort](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

Sort an array using RPG sorting rules.

```cs
void SortArr(Array arrayToSort)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | arrayToSort | The array to sort.

### void SortNonContiguosArr([Array baseArray](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0), [Array arrayToSort](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0))

Sort a base array using a second array as a key array, using RPG sorting rules. This method only sorts arrays of strings or arrays of decimal numbers.

```cs
void SortNonContiguosArr(Array baseArray, Array arrayToSort)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | baseArray | The array to sort.
| [Array](https://learn.microsoft.com/en-us/dotnet/api/system.array?view=net-8.0) | arrayToSort | The array of keys.

### void TestBits([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [string mask](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Boolean& off](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& on](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& eq](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Compares the bits in mask with the corresponding bits in b.

```cs
void TestBits(byte b, string mask, Boolean& off, Boolean& on, Boolean& eq)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | Input byte value.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | mask | Can contain: Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036'. A Character Expression. Hexadecimal literal (H'01') for example. Named constant up to 8 positions long containing the bit numbers to be set on.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | off | Reflects the status of the result field bits.  Assuming a Mask of H'E4' (1100 0100), Off is true if all of the masked bits are Off in the field.  In this case, for Off to be true, the field would contain H'3B' (0011 1011).
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | on | Reflects the status of the result field bits.  Assuming a Mask of H'E4' (1100 0100), On is true if some of the masked bits are On and some the masked bits are Off in the field.  In this case, the field would contain anything but H'3B' or H'E4'.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | eq | Reflects the status of the result field bits.  Assuming a Mask of H'E4' (1100 0100), Eq is true if all of the masked bits are On in the field.  In this case, the field would contain H'E4' (1100 0100)..

### void TestBitsWithByte([byte b](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [byte maskByte](https://docs.microsoft.com/en-us/dotnet/api/system.byte), [Boolean& off](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& on](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean& eq](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Compares the bits in maskByte with the corresponding bits in b.

```cs
void TestBitsWithByte(byte b, byte maskByte, Boolean& off, Boolean& on, Boolean& eq)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | b | Input byte value.
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | maskByte | Can contain: Bit numbers 0-7. Enclose the bit numbers in apostrophes. For example, to set bits 0, 3, 6 on, enter '036'. A Character Expression. Hexadecimal literal (H'01') for example. Named constant up to 8 positions long containing the bit numbers to be set on.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | off | Reflects the status of the result field bits.  Assuming a Mask of H'E4' (1100 0100), Off is true if all of the masked bits are Off in the field.  In this case, for Off to be true, the field would contain H'3B' (0011 1011).
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | on | Reflects the status of the result field bits.  Assuming a Mask of H'E4' (1100 0100), On is true if some of the masked bits are On and some the masked bits are Off in the field.  In this case, the field would contain anything but H'3B' or H'E4'.
| [Boolean&](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | eq | Reflects the status of the result field bits.  Assuming a Mask of H'E4' (1100 0100), Eq is true if all of the masked bits are On in the field.  In this case, the field would contain H'E4' (1100 0100).

### char ToChar([string sA](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the first character of a specified string to a Unicode character.

```cs
char ToChar(string sA)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sA | A string.

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | A Unicode character that is equivalent to the first character in sA. If sA is null or its length is 0, the return value is '0'.
