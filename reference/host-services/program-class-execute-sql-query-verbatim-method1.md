---
title: Program.ExecuteSQL_QueryVerbatim Method (string,DBParm[])

---

Executes a SQL query specifying the SQL statement (exactly as stated in the RPG code) and statement parameters.
<!-- start -->

#### Syntax
<pre class="syntax"> **BegFunc ExecuteSQL_QueryVerbatim Access(*Public) Type(System.Collections.Generic.Dictionary)
   DclSrParm *sqlText*  Type(*String)
   DclSrParm *parameters*  Type (DBParm) Rank(1)**       </pre>

#### Parameters
<dl>
        <dt>
 *sqlText* 
        </dt>
        <dd>String. The SQL statement
        with a substitution variable defined for each parameter.</dd>
        <dt>
 *parameters*  </dt>
        <dd>
          [
        DBParm](program-db-parm-class.html). An array containing the query parameters.</dd>
</dl>

#### Returns
**System.Collections.Generic.Dictionary** (string and object) representing the query results allowing values for a particular column to be accessed by name.
<!-- -->

 <!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](monarch-namespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Program Class](program-class.html) <br /> [Program Class Members](program-class-members.html) <br /> [ SqlQueryResults Field](program-class-sql-query-results-field.html) <br /> [ Program.DBParm Class](program-db-parm-class.html) <br /> [ASNA.Monarch Namespace](monarch-namespace.html) 
