---
title: FieldType.NewTimeStamp Method

---

Creates a new timestamp [ FieldType](field-type-class.html).

## Remarks

**NewTimeStamp** constructs a **FieldType** which represents a DataGate timestamp field. Timestamp fields contain calendar date and 24-hour clock time data denoting a specific instant in time. The storage size of a timestamp field is 26 bytes.

**Note** : Internally, DG manipulates date, time, and timestamp fields as **System.DateTime** value types. The object value returned by DG as the value of a date, time, or timestamp field (in methods such as [As400Program.ParmToObject](as400program-class-parm-to_object-method-main.html)) will be converted from a value of DateTime. Likewise, DG will only accept values which can be accurately converted to DateTime values, for setting the value of date, time, or timestamp fields.
## Examples


```cs 
  /* Use the already initialized As400OProgram "timeProg" to set the
   * value of a DateTime variable. This program accepts a timestamp data type
   * whose time format is ISO as its sole parameter, which it does not
   * read but uses to return data. */

  ProgParmType as400Time = new ProgParmType("TimeISO", 0, FieldType.NewTimestamp());
  ProgParm timeParm = new ProgParm(as400Time, DataDirection.Output);
  timeProg.AppendParm(timeParm);

  timeProg.Execute();

  DateTime currentTime;
  currentTime = Convert.ToDateTime(timeProg.ParmToObject(timeParm, Type.GetType("System.DateTime"), 0));
  /* Unlike the IBM i FieldType NewTime or NewDate, NewTimeStamp contains both date and time
   * values. */
```


## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FieldType Class](field-type-class.html)
      <br />
[FieldType Class Members](field-type-members.html)
      <br />
[As400Program.ParmToObject](as400program-class-parm-to_object-method-main.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

