---
title: CLProgram.OverrideFile Methods

---

This overloaded method provides CLProgram file override options. 

You can use an override command to replace the database file named in a CL procedure or program or to change certain parameters of the existing database file. These overrides can be applied to DBFile, PrintFile, or a WorkStnFile file. This may be especially useful for files that have been renamed or moved since the procedure or program was created. It can also be used to access a file member other than the first member. 

When you override to a different file(ToFile), the overriding file must have only one record format. A logical file, which has multiple record formats defined in DDS, may be used if it is defined over only one physical file member. A logical file, which has only one record format defined in the DDS, may be defined over more than one physical file member. The name of the format does not have to be the same as the format name referred to when the program was created. 

You should ensure that the format of the data in the overriding file is the same as in the original file, otherwise you may get unexpected results.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->

          <tr>
            <td>           <code>[
              OverrideFile (
 *string, OverrideOptions, object* )](clprogram-class-override-file-method1.html)</code>
            </td>
            <td>Overrides a 
 *CL procedure, program,
            or file*  for the 
 *option*  specified with a 
 *new value*  that is provided.</td>
          </tr>
          <tr>
            <td>              <code>[
              OverrideFile (
 *string, OverrideOptions, object,
              OverrideScope* )](clprogram-class-override-file-method2.html)</code>
            </td>
            <td>Overrides a 
 *CL procedure, program,
            or file*  for the 
 *option*  specified with a 
 *new value*  that is provided for the 
 *scope*  indicated (call level or job level).</td>
          </tr>
</table>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](monarch-namespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->      

#### See Also
[CLProgram Class](clprogram-class.html) <br clear="none" /> [ CLProgram Members](clprogram-class-members.html) <br clear="none" /> [ ASNA.Monarch.OverrideOptions](override-options-enumeration.html) <br clear="none" /> [ ASNA.Monarch.OverrideScope](overrideScope-enumeration.html) <br clear="none" /> [ASNA.Monarch Namespace](monarch-namespace.html) 
