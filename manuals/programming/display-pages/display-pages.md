---
title: "Expo Display Pages"
description: "Explore best practices for displaying pages on your website. Learn how to enhance user experience with responsive design and fast loading times."
---

An [Expo Display Page](/concepts/user-interface/qsys-expo-display-pages.html) is an ASP.NET RazorPage that uses ASNA.Expo TagHelpers to Render a Workstation file using a flexible Grid Layout suitable to present with fidelity a migrated IBM i Displayfile.

## Model

### QSys.Model Attributes
Monarch Base provides the following Attributes to assist in defining the data model Display Page.  All of these Tag Helpers reside in the ```ASNA.QSys.Expo.Model``` namespace. Even though their names end in ```Attribute```, it is the convention to omit this suffix.

#### File Level
DisplayPage

#### Record Level
Record

SubfileControl

SubfileRecord

#### Field Level
Byte

Char

Date

Dec

## View

### QSys.Expo Tag Helpers
Monarch Base provides the following Tag Helpers to assist in rendering the information on the Display Page Model.  All of these Tag Helpers reside in the ```ASNA.QSys.Expo.Tags``` namespace. Even though their names end in ```TagHelper```, it is the convention to omit this suffix. 

#### File Level
DdsFile

DdsFunctionKeys

DdsMessagePanel

#### Record Level

DdsButton

DdsRecord

DdsSubfileControl

DdsSubfileRecord


#### Field Level

Define a Constant with:
 * DdsConstant

Define Fields with these Tag Helpers:
 * DdsCharField
 * DdsCheckboxField
 * DdsDateField
 * DdsDecDateField
 * DdsDecField
 * DdsRadioButtonGroupField
 * DdsSignature

Locate an arbitrary HTML Element at a particular Row/Column position with:
 * Col
 * ColSpan
 * DdsGridRow


