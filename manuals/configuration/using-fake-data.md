---
title: "Using Fake Data"
description: "Discover how using fake data can accelerate development and testing. This guide covers benefits, tools, and best practices for effective use."
---


The `Display` section of the [website configuration](configure-expo-website.html#displaypages) provides the ability to create and utilize fake data.  Fake data is utilized when particular pages of the website are to be displayed but the user does not wish to navigate the application all the way to the page.  This feature can be used by a developer to provide a set of files to another developer working purely in the look and feel of the website.

The section has these two properties:
 - `FakeDataType` - Valid values: `None`, `Output`, `Input`
 - `FakeDataDirectory` - Directory where Fake data files are located. It may be an absolute path or relative to the web site.

When `FakeDataType` is equal to `None`, then no fake data is involved in the process.

## Creating Fake Data
Setting the `FakeDataType` value to `Input` will allow the Website to run normally with the addition of a button, named `Save FakeData`, added to the function key pad allowing the developer to save the dataset used to produced the page to the `FakeDataDirectory`.  The `.fake` file is created with the same name as the current page being displayed. If a `.fake` file already exists in the directory then a numeric prefix is appended to the name of the file.


For this example, assume `appsettings.json` has this entry:
```json
  "DisplayPages": {
    "FakeDataType": "Input",
    "FakeDataDirectory": "./FakeData"
  },
  ```
Further assume the website is showing a page called 'ORDER' in an Area called 'Sales'. 

Clicking the `Save FakeData` button will produce a file with the values of the currently displayed records, fields and indicators. The file would placed at this location at the root of the website:

     `FakeData/Sales/ORDER.fake`

If a second time the `Save FakeData` button is clicked, the file would be named:

     `FakeData/Sales/ORDER-1.fake`

And if a third time the button is clicked, then the file would be called:
     
     `FakeData/Sales/ORDER-2.fake`

A `.fake` file can also be created or edited using any editor suitable for XML.

## Displaying Fake Data
Setting the `FakeDataType` configuration value to `Output` will let Expo know to **not** call the Job's logic but instead to display pages with data coming from the `FakeDataDirectory`.  The directory should have one `.fake` XML file for each Display Page that is to be displayed.  If a `.fake` file is not found, Expo will create one with default data. The content of the `.fake` files is the XML version of the Dataset for the page.

Using the example above, but with this configuration 
```json
  "DisplayPages": {
    "FakeDataType": "Output",
    "FakeDataDirectory": "./FakeData"
  },
  ```
would allow a user to enter the URL to the ORDER page directly without having to navigate the application to the program using the ORDER display file. So entering this address on the browser

     //MySite/Sales/ORDER

would show the page with the data from 

     `FakeData/Sales/ORDER.fake`

When using fake data for output, the query string parameter `FakeDataSetId` can be passed to specify a suffix for the `.fake` data file name. The suffix  is appended, separated by a hyphen, to the name of the razor page when looking for an existing `.fake` data file.

Entering the following address on the browser

     //MySite/Sales/ORDER?FakeDataSetId=2

would show the page with data from 

     `FakeData/Sales/ORDER-2.fake`

The value of FakeDataSetID can be any string.  For instance, you could pass 

    //MySite/Sales/ORDER?FakeDataSetId=TestXYZ

and the fetched file would be

     `FakeData/Sales/ORDER-TestXYZ.fake`

If the file being fetched does not exists, one is created with generated data.
