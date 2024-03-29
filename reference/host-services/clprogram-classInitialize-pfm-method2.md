---
title: CLProgram.InitializePFM(string, string, integer)

---

Initializes records in a member of a physical file with default record values, to the total number of records specified.

#### Syntax
<pre class="syntax"> **BegSr InitializePFM Access(*Protected) Type(Void)
   DclSrParm *File*  Type(*String)
   DclSrParm *Mbr*  Type(*Integer)
   DclSrParm *TotRcds*  Type(*Integer4)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *File* </code>
        </dt>
        <dd>

String. The qualified name of the physical file containing the member to initialize. The name of the physical file can be qualified by one of the following library values:

- <code><u>*LIBL</u></code>: All libraries in the job's library
            list are searched until the first match is found. This
            is the default.
- <code>*CURLIB</code>: The current library for the
            job is searched. If no library is specified as the
            current library for the job, the <code>QGPL</code> library is
            used.
- <code> *library-name* </code>: Specify the name of the library
            to be searched.
- <code> *physical-file-name* </code>: Specify the name of the
            physical file.

</dd>
        <dt>
         <code> *Mbr* </code>
        </dt>
        <dd>

String. The optional name of the physical file member within the *File* to be initialized. The name of the member can be:

- <code><u>*FIRST</u></code>: The first member in the database file is
            initialized. This is the default.
- <code>*LAST</code>: The last member of the
            database file is initialized.
- <code> *physical-file-member* </code>: Specify the name of the
            physical file member.

</dd>
        <dt>
          <code> *TotRcds* </code>
        </dt>
        <dd>

Integer8. Specifies the total number of records in the member after it is initialized. If the value specified in this parameter causes the size of the file to be larger than the size specified when the file was created, a message is sent to the system operator's message queue (<code>QSYSOPR</code>). The operator can either continue or end the operation. If the number of existing records in the member already meets or is larger than this number, no records are initialized; if the number is less than that specified, enough records are initialized to equal the total records specified.
</dd>
</dl>

#### Remarks
This method initializes records in a member of a physical file to default record values. Numeric fields are initialized to zeros and all character fields are initialized to blanks. If the initialized member is empty, records are added and initialized; if the member is not empty, records are added to the member. As many records are added as is necessary to make the total record count specified.

**The following restrictions apply:** 

- The member may be open for input (read-only) while the
        initialize operation takes place but cannot be open for
        update, delete, or insert.
- To initialize the member with default records, the user
        needs object operational authority, object management
        authority or alter, and add authority for the file in which
        the member exists and execute authority to the
        library.
- To initialize the member with deleted records, the user
        also needs delete authority for the file.
- An *EXCLRD lock is required on the member to initialize
        it.
- In multithreaded jobs, this command is not thread safe
        and fails for Distributed Data Management (DDM) files of
        type *SNA.

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](monarch-namespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->      

#### See Also
[CLProgram Class](clprogram-class.html) <br clear="none" /> [ CLProgram Class Members](clprogram-class-members.html) <br clear="none" /> [ASNA.Monarch Namespace](monarch-namespace.html) 
