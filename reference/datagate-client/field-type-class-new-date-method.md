---
title: FieldType.NewDate Method

---

Creates a new date [ FieldType](field-type-class.html).

## Parameters



 *fmt* 

: 
[DateTimeFormat](date-time-format-enumeration.html).  The format 
						of the date field.


## Exceptions

System.ArgumentException.  Thrown if *fmt*  is **DateTimeFormat.HMS** .

## Remarks

**NewDate** constructs a **FieldType** that represents a DataGate date field. Date fields contain calendar date data in a variety of formats, as specified by *fmt* . The storage size of a date field is 6 to 10 bytes, dependent upon the format (see [ DateTimeFormat](date-time-format-enumeration.html) for details).

The value of *fmt* may be any value of **DateTimeFormat** , except for **HMS** .

Note that internally, DG manipulates date, time, and timestamp fields as **System.DateTime** value types. The object value returned by DG as the value of a date, time, or timestamp field (in methods such as [ As400Program.ParmToObject](as400program-class-parm-to_object-method-main.html)) will be converted from a value of **DateTime** . Likewise, DG will only accept values which can be accurately converted to **DateTime** values, for setting the value of date, time, or timestamp fields.
## Examples


```cs 
  /* Create a parms list to pass to a pre-initialized As400Program object.
   * We want to pass one date with time format *USA and another with time
   * format *ISO. Other time formats are available in the DateTimeFormat
   * enumeration as well. */
  DateTime DateUSA = System.DateTime.Now;
  DateTime DateISO = System.DateTime.Now;

  ProgParmType type1 = new ProgParmType("DateUSA", 0, FieldType.NewDate(DateTimeFormat.USA));
  ProgParmType type2 = new ProgParmType("DateISO", 0, FieldType.NewDate(DateTimeFormat.ISO));
  ProgParm parm1 = new ProgParm(type1, DataDirection.InputOutput);
  ProgParm parm2 = new ProgParm(type2, DataDirection.InputOutput);

  prog.AppendParm(parm1);
  prog.AppendParm(parm2);

  /* In the lines below, we assign the IBM i program parameters
   * values from our .NET variables. */
  prog.ObjectToParm(parm1, DateUSA, 0);
  prog.ObjectToParm(parm1, DateISO, 0);

  /* Call the program. */
  prog.Execute();

  /* The parameters can be bidirectional and thus return data as well. 
   * To use that data, we assign the values of the parameters back to our
   * .NET variables. */
  DateUSA = Convert.ToDateTime(prog.ParmToObject(parm1, DateUSA.GetType(), 0));
  DateISO = Convert.ToDateTime(prog.ParmToObject(parm2, DateUSA.GetType(), 0));
  /* IMPORTANT NOTE: The time and date data types do not return all the information
   * which a .NET DateTime can contain. Specifically, if you specify a parm as a NewTime,
   * the data portion of the returned DateTime will be set to MinValue. The same will
   * happen to the time portion of a variable if its IBM i parm was set to be a NewDate. */
```


## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html)

<span> **Assembly:** ASNA DataGate Client</span>

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also

[FieldType Class](field-type-class.html)<br />[FieldType Class Members](field-type-members.html)<br />[DateTimeFormat Enumeration](date-time-format-enumeration.html)<br />[As400Program.ParmToObject](as400program-class-parm-to_object-method-main.html)
 <br />[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

