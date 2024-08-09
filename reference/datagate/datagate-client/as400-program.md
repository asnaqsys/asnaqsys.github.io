---
title: "As400Program class            | QSYS API Reference Guide"
description: "Represents a program in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents a program in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

## Remarks
This class provides methods and properties to manage a program in the ASNA DataGate client. 
It includes methods to set the program path and connection, execute the program, 
get and append parameters, convert parameters to and from objects, set parameters to zero value, 
and read and write parameters in XML format. It also implements the IDisposable interface, 
which provides a mechanism for releasing unmanaged resources.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [As400Program()](#as400program) | Initializes a new instance of the  class.
| [As400Program](#as400programadgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the  class with the specified connection.
| [As400Program](#as400programadgconnection-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified connection and program path.

### As400Program()

Initializes a new instance of the  class.

```cs
As400Program()
```

### As400Program([AdgConnection](/reference/datagate/datagate-client/adg-connection.html))

Initializes a new instance of the  class with the specified connection.

```cs
As400Program(AdgConnection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to be used by the program.

### As400Program([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the  class with the specified connection and program path.

```cs
As400Program(AdgConnection, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to be used by the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | programPath | The path of the program to be executed.

## Methods

| Signature | Description |
| --- | --- |
| [AppendParm](#void-appendparmprogparm-parameter)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends a parameter to the program.
| [AppendParm](#void-appendparmprogparm-parameter)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends a parameter to the specified list of parameters.
| [AppendParms](#void-appendparmsprogparm--parameters)([ProgParm\[\]](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends an array of parameters to the program.
| [Dispose()](#void-dispose) | Releases all resources used by the current instance of the  class.
| [Dispose](#void-disposebool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the unmanaged resources used by the  and optionally releases the managed resources.
| [Execute()](#void-execute) | Executes the program with the current parameters.
| [Finalize()](#void-finalize) | Finalizes an instance of the  class.
| [GetParameters()](#ienumerable-progparm-getparameters) | Gets the parameters of the program.
| [GetParmByName](#progparm-getparmbynamestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the parameter with the specified name.
| [GetParmByName](#progparm-getparmbynamestring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the parameter with the specified name from the specified list of parameters.
| [ObjectToParm](#void-objecttoparmprogparm-parameter-object-value-int-element)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified object to a parameter of the specified type.
| [ObjectToParm](#void-objecttoparmprogparm-parameter-object-value)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Converts the specified object to a parameter.
| [ObjectToParm](#void-objecttoparmobject-value-string-parametername-int32--elementindices)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified object to a parameter of the specified name and element indices.
| [ObjectToParm](#void-objecttoparmobject-value-string-parametername)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified object to a parameter of the specified name.
| [ParmToObject](#object-parmtoobjectprogparm-parameter-type-returntype-int-element)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified parameter to an object of the specified type.
| [ParmToObject](#object-parmtoobjectprogparm-parameter-type-returntype)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Converts the specified parameter to an object of the specified type.
| [ParmToObject](#object-parmtoobjecttype-returntype-string-parametername-int32--elementindices)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts the specified parameter to an object of the specified type.
| [ParmToObject](#object-parmtoobjecttype-returntype-string-parametername)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts the specified parameter to an object of the specified type.
| [ReadParmXml](#void-readparmxmlxmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Reads the parameters of the program from an XML reader.
| [SetConnection](#void-setconnectionadgconnection-value)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Sets the connection to be used by the program.
| [SetParmsZeroValue()](#void-setparmszerovalue) | Sets all parameters of the program to their zero value.
| [SetProgramPath](#void-setprogrampathstring-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the path of the program to be executed.
| [WriteParmXml](#void-writeparmxmlxmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Writes the parameters of the program to an XML writer.

### void AppendParm([ProgParm parameter](/reference/datagate/datagate-data-link/prog-parm.html))

Appends a parameter to the program.


#### Remarks
This method appends a parameter to the program in the ASNA DataGate client. It checks if the provided parameter is null, and if so, throws an ArgumentNullException. It then adds the parameter to the list of parameters for the program.

```cs
void AppendParm(ProgParm parameter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to append.

### void AppendParm([ProgParm parameter](/reference/datagate/datagate-data-link/prog-parm.html))

Appends a parameter to the specified list of parameters.


#### Remarks
This method appends a parameter to the specified list of parameters in the ASNA DataGate client. It checks if the provided parameter is named, and if not, throws an ArgumentException. It also checks if a parameter with the same name already exists in the list, and if so, throws an ArgumentException. It then adds the parameter to the list.

```cs
void AppendParm(ProgParm parameter)
```

### void AppendParms([ProgParm\[\] parameters](/reference/datagate/datagate-data-link/prog-parm.html))

Appends an array of parameters to the program.


#### Remarks
This method appends an array of parameters to the program in the ASNA DataGate client. It checks if the provided array is null, and if so, throws an ArgumentNullException. It then iterates over the array and appends each parameter to the program using the AppendParm method.

```cs
void AppendParms(ProgParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm\[\]](/reference/datagate/datagate-data-link/prog-parm.html) | parameters | The array of parameters to append.

### void Dispose()

Releases all resources used by the current instance of the  class.


#### Remarks
This method calls the Dispose method with the isDisposing parameter set to true, indicating that the method has been called directly or indirectly by a user's code. Then it requests that the common language runtime not call the finalizer for the specified object.

```cs
void Dispose()
```

### void Dispose([bool isDisposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the unmanaged resources used by the  and optionally releases the managed resources.


#### Remarks
This method is called by the public Dispose() method and the Finalize method. Dispose() invokes the protected Dispose() method with the isDisposing parameter set to true. Finalize invokes Dispose with isDisposing set to false.When the isDisposing parameter is true, this method releases all resources held by any managed objects that this As400Program references. This method invokes the Dispose() method of each referenced object.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | True to release both managed and unmanaged resources; false to release only unmanaged resources.

### void Execute()

Executes the program with the current parameters.


#### Remarks
This method executes the program in the ASNA DataGate client. It first checks if the program path is null or empty, and if so, throws an InvalidOperationException. It then creates a new ParmExchanger with the current parameters and calls the program with the ParmExchanger. The ParmExchanger writes the parameters to the data link before the program is called and reads the parameters from the data link after the program is called.

```cs
void Execute()
```

### void Finalize()

Finalizes an instance of the  class.


#### Remarks
This finalizer calls the Dispose method with the isDisposing parameter set to false, indicating that the method has been called by the runtime and not from the Dispose method.

```cs
void Finalize()
```

### IEnumerable<ProgParm> GetParameters()

Gets the parameters of the program.


#### Remarks
This method returns a read-only collection of the parameters of the program in the ASNA DataGate client. The parameters are stored in a list, which is converted to a read-only collection before being returned.

```cs
IEnumerable<ProgParm> GetParameters()
```

### ProgParm GetParmByName([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the parameter with the specified name.


#### Remarks
This method returns the parameter with the specified name in the ASNA DataGate client. The name comparison is case-insensitive. If no such parameter exists, it returns null.

```cs
ProgParm GetParmByName(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.

#### Returns

| Type | Description
| --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | The parameter with the specified name, or null if no such parameter exists.

### ProgParm GetParmByName([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the parameter with the specified name from the specified list of parameters.


#### Remarks
This method returns the parameter with the specified name from the specified list of parameters in the ASNA DataGate client. The name comparison is case-insensitive. If no such parameter exists, it returns null.

```cs
ProgParm GetParmByName(string name)
```

### void ObjectToParm([ProgParm parameter](/reference/datagate/datagate-data-link/prog-parm.html), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object), [int element](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts the specified object to a parameter of the specified type.


#### Remarks
This method converts the specified object to a parameter of the specified type in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then creates a new SubParmName with the specified element index and calls the FromObject method of the parameter with the SubParmName and the object.

```cs
void ObjectToParm(ProgParm parameter, object value, int element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to convert the object to.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | element | The index of the element to convert, if the parameter is an array.

### void ObjectToParm([ProgParm parameter](/reference/datagate/datagate-data-link/prog-parm.html), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Converts the specified object to a parameter.


#### Remarks
This method converts the specified object to a parameter in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then calls the ObjectToParm method with the parameter, object, and an element index of 0.

```cs
void ObjectToParm(ProgParm parameter, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to convert the object to.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.

### void ObjectToParm([object value](https://docs.microsoft.com/en-us/dotnet/api/system.object), [string parameterName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Int32\[\] elementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts the specified object to a parameter of the specified name and element indices.


#### Remarks
This method converts the specified object to a parameter of the specified name and element indices in the ASNA DataGate client. It checks if the provided parameter name is null, and if so, throws an ArgumentNullException. It then creates a new SubParmName with the specified parameter name and element indices, and gets the parameter with the name from the SubParmName. If no such parameter exists, it throws an ArgumentException. It then calls the FromObject method of the parameter with the SubParmName and the object.

```cs
void ObjectToParm(object value, string parameterName, Int32[] elementIndices)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameterName | The name of the parameter to convert the object to.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | elementIndices | The indices of the elements to convert, if the parameter is an array.

### void ObjectToParm([object value](https://docs.microsoft.com/en-us/dotnet/api/system.object), [string parameterName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the specified object to a parameter of the specified name.


#### Remarks
This method converts the specified object to a parameter of the specified name in the ASNA DataGate client. It calls the ObjectToParm method with the object, parameter name, and an empty array of element indices.

```cs
void ObjectToParm(object value, string parameterName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameterName | The name of the parameter to convert the object to.

### object ParmToObject([ProgParm parameter](/reference/datagate/datagate-data-link/prog-parm.html), [Type returnType](https://docs.microsoft.com/en-us/dotnet/api/system.type), [int element](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Converts the specified parameter to an object of the specified type.


#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then creates a new SubParmName with the specified element index and calls the ToObject method of the parameter with the SubParmName.

```cs
object ParmToObject(ProgParm parameter, Type returnType, int element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | returnType | The type to convert the parameter to.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | element | The index of the element to convert, if the parameter is an array.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

### object ParmToObject([ProgParm Parameter](/reference/datagate/datagate-data-link/prog-parm.html), [Type ReturnType](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Converts the specified parameter to an object of the specified type.


#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then creates a new SubParmName with the specified element index and calls the ToObject method of the parameter with the SubParmName.

```cs
object ParmToObject(ProgParm Parameter, Type ReturnType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Parameter | The parameter to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert the parameter to.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

### object ParmToObject([Type returnType](https://docs.microsoft.com/en-us/dotnet/api/system.type), [string parameterName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Int32\[\] elementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts the specified parameter to an object of the specified type.


#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It checks if the provided parameter name is null, and if so, throws an ArgumentNullException. It then creates a new SubParmName with the specified parameter name and element indices, and gets the parameter with the name from the SubParmName. If no such parameter exists, it throws an ArgumentException. It then calls the ToObject method of the parameter with the SubParmName and the type.

```cs
object ParmToObject(Type returnType, string parameterName, Int32[] elementIndices)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | returnType | The type to convert the parameter to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameterName | The name of the parameter to convert.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | elementIndices | The indices of the elements to convert, if the parameter is an array.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

### object ParmToObject([Type ReturnType](https://docs.microsoft.com/en-us/dotnet/api/system.type), [string ParameterName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Converts the specified parameter to an object of the specified type.


#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It calls the ParmToObject method with the type, parameter name, and an empty array of element indices.

```cs
object ParmToObject(Type ReturnType, string ParameterName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert the parameter to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParameterName | The name of the parameter to convert.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

### void ReadParmXml([XmlReader reader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0))

Reads the parameters of the program from an XML reader.


#### Remarks
This method reads the parameters of the program in the ASNA DataGate client from an XML reader. It checks if the provided XML reader is null, and if so, throws an ArgumentNullException. It also checks if the read state of the XML reader is not Initial, and if so, throws an ArgumentException. It then reads the "apcml" and "program" elements from the XML. If the "program" element is not found, it throws an XmlException. It then reads the name attribute of the "program" element and creates a new list of parameters. It then reads each parameter from the XML using the ProgParm constructor, appends it to the list, and creates a new buffer for it. It then reads the end of the "program" and "apcml" elements and closes the XML reader, and sets the program name and parameters to the new values.

```cs
void ReadParmXml(XmlReader reader)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The XML reader to read from.

### void SetConnection([AdgConnection value](/reference/datagate/datagate-client/adg-connection.html))

Sets the connection to be used by the program.


#### Remarks
This method sets the connection for the ASNA DataGate client. The provided connection is checked for null before being set.

```cs
void SetConnection(AdgConnection value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | value | The connection to be used.

### void SetParmsZeroValue()

Sets all parameters of the program to their zero value.


#### Remarks
This method sets all parameters of the program in the ASNA DataGate client to their zero value. It iterates over the list of parameters and calls the SetZeroValue method of each parameter.

```cs
void SetParmsZeroValue()
```

### void SetProgramPath([string value](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the path of the program to be executed.


#### Remarks
This method sets the program path for the ASNA DataGate client. The provided path is converted to upper case invariant culture before being set.

```cs
void SetProgramPath(string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The path of the program.

### void WriteParmXml([XmlWriter writer](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0))

Writes the parameters of the program to an XML writer.


#### Remarks
This method writes the parameters of the program in the ASNA DataGate client to an XML writer. It checks if the provided XML writer is null, and if so, throws an ArgumentNullException. It also checks if the write state of the XML writer is not Start, and if so, throws an ArgumentException. It then writes the start of the document, the start of the "apcml" element with the appropriate namespace and version attribute, the start of the "program" element with the program name attribute, and the XML representation of each parameter using the WriteXml method of the parameter. It then writes the end of the "program" and "apcml" elements and the end of the document, and closes the XML writer.

```cs
void WriteParmXml(XmlWriter writer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.

## Example 1. As400Program constructor method example.

```cs 
  /* Here, "ProdDB" is an initialized AdgConnection and
   * Call400 is a valid IBM i program file. */
  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");
```

## Example 2. As400Program constructor method example 2.

```cs 
  //Here, "ProdDB" is an initialized AdgConnection.
  As400Program prog = new As400Program(ProdDB);
  prog.SetProgramPath( "*Libl/Call400" );
```

## Example 3. As400Program constructor method example 3.

```cs 
  //Here, "ProdDB" is an initialized AdgConnection.
  As400Program prog = new As400Program();
  prog.SetConnection( ProdDB );
  prog.SetProgramPath("*Libl/Call400");
```

## Example 4. ParmToObject method example.

```cs 
  /* Here, Prog is an initialized As400Program object
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[3];
  Parms[0] = new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output);
  Parms[1] = new ProgParm(
        new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output);
  Parms[2] = new ProgParm(
        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input);
  prog.AppendParms(Parms);
  prog.ObjectToParm(Parms[2], Quit400App, 0);
  prog.Execute(); 
  /* After calling the last two values in the parameter list
   * will have new values in it.  To read them, we set our local
   * variables to the returned values in the parameters list. */
  CustName = Convert.ToString(
      prog.ParmToObject(System.Type.GetType("System.String"),
      "CustName",
      0));
  TimeOfDay = Convert.ToDecimal( prog.ParmToObject(System.Type.GetType("System.Decimal"),
      "TimeOfDay",
       0));
```

## Example 5. ObjectToParm method example.

```cs 
  /* Here, "prog" is an initialized As400Program object.
   * The first two lines creates a IBM i character data type whose
   * length is one, and then appends it to "prog"'s parameter list. */
  ProgParm QuitParm = new ProgParm(
        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
        DataDirection.InputOutput );
  prog.AppendParm(QuitParm);
  char QuitChar = '1';
  /* This next line assigns the .NET value, CustName, to the
   * IBM i data type of the same name in the parameter list. */
  prog.ObjectToParm(QuitParm, QuitChar, 0);

```

## Example 6. as400Program Connection property example.

```cs 
  As400Program prog = new As400Program();
  prog.SetConnection( new AdgConnection("*Public/DG NET IBM i") );
  prog.SetProgramPath( "*Libl/Call400" );
```


## Example  7. as400Program AppendParms method example.

```cs 
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
      DataDirection.Input)
  };
  prog.AppendParms(Parms);
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  prog.Execute();
  CustName = Convert.ToString(
     prog.ParmToObject(System.Type.GetType("System.String"),
     "CustName",
     new int[]{}));
  TimeOfDay = Convert.ToDecimal(
     prog.ParmToObject(System.Type.GetType("System.Decimal"),
     "TimeOfDay",
     new int[]{}));
             
```

## Example 8. as400Program AppendParm method example.

```cs 
  /* Here, prog is an initialized As400Program.
   * We add the field "CustName" to the parm list, and a local
   * string variable by the same name into it.  After calling the
   * program, we then set the local variable to the returned
   * value in the parms list. */
  prog.AppendParm( new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)),
        DataDirection.InputOutput
  ));
  //Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", new int[]{} );
  prog.Execute();
  //Fetch the returned value.
  CustName = Convert.ToString(
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", 
        new int[]{}));  
```


## Example 9. as400Program SetProgramPath method example.

```cs 
  As400Program prog = new As400Program();
  prog.SetConnection( new AdgConnection("*Public/DG NET IBM i") );
  prog.SetProgramPath = "*Libl/Call400";
```
