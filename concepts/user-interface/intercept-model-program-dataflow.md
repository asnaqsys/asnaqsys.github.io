---
title: "Intercept Model to Program (and back) Data Flow Guide"
description: "Uncover the dynamics of the intercepting Model and Program Data Flow with this insightful guide." 
---

Sometimes it is desirable to introduce changes in the UI without affecting the Application Logic.

This is particularly important when enhancing the UI on a [ASNA Wings](https://docs.asna.com/documentation/Help170/Wings/_HTML/Welcome.htm) deployment.

The [DisplayPageModel class](/reference/expo/qsys-expo-model/display-page-model.html) plays an important role as the UI Controller, and its responsible for sending and receiving the UI Data *to* the Application Logic and *from* the User (Browser response).

There are two virtual methods on [DisplayPageModel class](/reference/expo/qsys-expo-model/display-page-model.html) that allow us to *intercept* the Data that is flowing from the the Application to the User *or* from User to the Application:

1. `OnCopyDisplayfileToBrowser`: right before the Application data is sent to the User (Browser) 
2. `OnCopyBrowserToDisplayFile`: right before the User (Browser) response is sent back to the Application.

## Convenience Methods available to access Data and Indicators

To intercept (and possibly modify) the data while its flowing from/to the Application or from/to the User response (Browser), you start by overriding the desired method.

```cs
protected override void OnCopyDspFileToBrowser()
{
    base.OnCopyDspFileToBrowser();

    // Do your changes to the data here, before the Page is rendered
}

protected override void OnCopyBrowserToDspFile()
{
    base.OnCopyBrowserToDspFile();

    // Do your changes to the data here, after the Dataset has been populated, right 
    // before the DataSet is sent to the Application Logic.
}
```

In Either case, you want to make sure that a particular record (including subfile) is *Active* (*has been written to* by the Application).

A. To check for a record being *Active* use read-only property `IsActive`, for example:

```cs
protected override void OnCopyDspFileToBrowser()
{
    base.OnCopyDspFileToBrowser();

    if ( CUSTREC.IsActive )
    {
        // Make your changes here.
    }
}

```

B. To find out how many records have been written to a Subfile, use `Count` read-only property.

```cs
protected override void OnCopyDspFileToBrowser()
{
    base.OnCopyDspFileToBrowser();

    if ( SFLC.IsActive && // My Subfile Controller is Active
         SFLC.SFL1.Count > 0 && SFLC.SFL1[0].IsActive ) // First record on the Subfile is Active
    {

    }
}
```


C. To get or set values from individual record fields, access directly the field by name:

```cs
    if ( CUSTREC.IsActive )
    {
        CUSTREC.SFCITY = "San Antonio";
    }
```

In the case of Subfile records, use indexer to get to proper field:

```cs
    if ( SFLC.IsActive && SFLC.SFL1.Count> 0 && SFLC.SFL1[0].IsActive ) 
    {
        SFLC.SFL1[0].SFSEL = 2;
    }
```

## Testing or Modifying Record Indicators.

There are two kind of indicators that are involved in Display Pages:
1. Option indicators.

    [IBM i DDS Manual](https://www.ibm.com/docs/en/i/7.5?topic=44-condition-display-files-positions-7-through-16), defines **Option** indicators as those that are placed in columns seven thru sixteen to *condition* Keywords and Fields. Syntax exist to combine indicators using logical operators such as **AND** and **OR**. When a keyword or field is conditioned and the expression evaluates to *True*, then the keyword is applied (if condition precedes a keyword) or the field is present/visible (if condition precedes a field definition). Otherwise (if expression is *False*), the keyword is ignored or the field is not included.

    >Option indicators are two-state values. At the time of writing the record an indicator can be either *set* or *reset* (true or false).

2. Response indicators. 

    A response indicator is defined as part of a [DDS keyword entries](https://www.ibm.com/docs/en/i/7.5?topic=ddf-dds-keyword-entries-display-files-positions-45-through-80), indicating that the *function* it represents has *completed*. Not all of the DDS Keywords may define a response indicator.

    >Response indicators are three-state values. When the *function* associated with the keyword executes, the response indicator can direct the indicator to be *set*, *reset* or *remain unchanged*. [Expo Model](/reference/expo/qsys-expo-model/landing-page-namespace.html) represents these three states as the characters: '1', '0' or 'X'.


When writing code inside the two overridden methods described above, an **Option indicator** may be tested as follows:

```cs

    // *IN61 was true when record was written.
    if (CUSTREC.GetOptionIndicator(61) ) 
    {

    }
```

Or a **Response indicator** may be tested in code, like:

```cs
    // Subfile record RRN 4 has changed, setting *IN03 to true. This is assuming that ChangeIndicator is defined on this record.
    if (SFLC.SFL1[3].GetResponseIndicator(3) == '1')
    {

    }
```

To change the value of Indicators, the [RecordModel class](/reference/expo/qsys-expo-model/record-model.html) provides the following two methods:

```cs
SetOptionIndicator(int indicator, bool newValue)

SetResponseIndicator(int indicator, char newValue01X)
```

Additionally if **ALL** the *one-hundred* indicators are needed, the following [RecordModel class](/reference/expo/qsys-expo-model/record-model.html) methods can be used to return *A Copy* of the indicator array:

```cs
bool[] GetOptionIndicators()

char[] GetResponseIndicators()
```

## Direct Access to the DataSet

The [DisplayPageModel class](/reference/expo/qsys-expo-model/display-page-model.html) provides methods to access the DataSet internal DataTable for advanced customization:

```cs
DataTable GetDataTable(string formatName)             // Access to DataTable for any active record (including subfile records)

DataRow GetDataRow(string formatName)                 // Access to DataRow for any active record (non-subfile)

DataRow GetSubfileDataRow(string formatName, int RRN) // Access to DataRow for any active subfile record (requires subfile-record RRN)
```


<br>

>The use of these Intercepting Data during User Interface operations is considered an **Advanced** topic. It requires a good knowledge of the [Monarch User Interface  Concepts](https://asnaqsys.github.io/concepts/user-interface/ui-overview.html). The methods described in this topic have some validation regarding the state of the Page Model, but it is your responsibility to make good use of them.
