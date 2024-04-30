---
title: MiscMessages class
---

A strongly-typed resource class, for looking up localized strings, etc.

**Namespace:** ASNA.DataGate.Client.Properties
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
|  | ResourceManager | Returns the cached ResourceManager instance used by this class. |
|  | Culture | Overrides the current thread's CurrentUICulture property for allresource lookups using this strongly typed resource class. |
|  | AdgConnection_DatabaseAlreadyOpen | Looks up a localized string similar to Database already open. |
|  | AdgConnection_DatabaseNotOpen | Looks up a localized string similar to Database not open. |
|  | AdgConnection_ShadowSourceProfileFailure | Looks up a localized string similar to SourceProfile serialization failed during prior connection close, possibly due to user impersonation.  For secure serialization in the thread impersonation scenario, the impersonated user profile must be loaded.  An alternative solution is to create a new AdgConnection object instead of re-opening a closed object.  See also the inner exception.. |
|  | AdgKeyUtils_CompareDeletedRow | Looks up a localized string similar to Can't compare deleted row.. |
|  | AdgObject_ValidationError | Looks up a localized string similar to XML validation failure: details in inner exception.. |
|  | As400Program_CnxDisposed | Looks up a localized string similar to Connection. |
|  | As400Program_DupParmName | Looks up a localized string similar to parm name collision. |
|  | As400Program_NoCnx | Looks up a localized string similar to Connection not set. |
|  | As400Program_ParmNotFound | Looks up a localized string similar to Parameter not found. |
|  | As400Program_ProgElemExpected | Looks up a localized string similar to <program> element not found. |
|  | As400Program_ProgramPathInvalid | Looks up a localized string similar to ProgramPath property not valid. |
|  | As400Program_StructParm | Looks up a localized string similar to struct Parameter. |
|  | As400Program_WriteStateNotStart | Looks up a localized string similar to XmlWriter.WriteState != Start. |
|  | BlockDataLink_UpreparedBuffer | Looks up a localized string similar to Accessing an invalid record buffer.. |
|  | ChannelOutputStream_NotPreparedExc | Looks up a localized string similar to ChannelOutputStream not Prepared. |
|  | ClientMonitor_Kill_DelayLessThanZero | Looks up a localized string similar to Delay must be greater than or equal to zero.. |
|  | ClientSecurity_ContextError | Looks up a localized string similar to server and security exceptions occurred. |
|  | ColumnConverters_ReaderUnavailable | Looks up a localized string similar to Accessing SQL '{0}' column '{1}' with .NET type '{2}' is not supported.. |
|  | CopyFromImportFile_ExpectCloseQuote | Looks up a localized string similar to Expecting closing string quote but hit end of file.. |
|  | DataAreaHelper_ImportFail | Looks up a localized string similar to Data area definition import failure.. |
|  | DataAreaHelper_ParmCollision | Looks up a localized string similar to Data area composition name collision.. |
|  | DataAreaHelper_ParmNotFound | Looks up a localized string similar to Data area composition name not found.. |
|  | DataAreaHelper_StructNotExpected | Looks up a localized string similar to Data area composition not expected.. |
|  | DatabaseName_ConfigTypeNotFound | Looks up a localized string similar to Database names cannot be used with this version of .NET.. |
|  | DatabaseName_NoNamesForExport | Looks up a localized string similar to No database names specified.. |
|  | DatabaseName_NoRegistry | Looks up a localized string similar to Registry-based database names are not supported on this platform.. |
|  | DgDateTimeConverter_DttExpected | Looks up a localized string similar to Expected valid date/time/timestamp field type.. |
|  | DgSHA_NotInitialized | Looks up a localized string similar to Must call Initialize() first.. |
|  | DirectoryHelper_NotDir | Looks up a localized string similar to IDirectory expected.. |
|  | DotNetProg_KeyNotInt | Looks up a localized string similar to Expected int-valued key.. |
|  | Expression_ParseErrors | Looks up a localized string similar to One or more errors occurred while parsing select/omit expressions.. |
|  | FieldType_ExtendedPropertiesMissing | Looks up a localized string similar to DataColumn is missing a DataGate ExtendedProperties entry.. |
|  | FieldType_InvalidPrintFieldDataType | Looks up a localized string similar to Print field has invalid data field type.. |
|  | FieldType_UnsupportedColumnDataTypeFormat | Looks up a localized string similar to Data type '{0}' of DataColumn '{1}' is not supported by DataGate.. |
|  | FileAdapter_FileNameSetException | Looks up a localized string similar to Connection is null; the Connection property must have a valid value before setting the value of FileName.. |
|  | FileAdapter_OpenQBadKeys | Looks up a localized string similar to key names and usage not coherent. |
|  | FileAdapter_OpenQBadQuery | Looks up a localized string similar to null query string or query file path. |
|  | FileAdapter_OpenQKeySpecFmt | Looks up a localized string similar to key name array element {0} cannot be null or empty string. |
|  | FileObjectHelper_FileNotFound | Looks up a localized string similar to File not found. |
|  | FileOpenAttr_TooManyFormats | Looks up a localized string similar to Format limits exceeded.. |
|  | Generic_InvalidArrayRegionParameters | Looks up a localized string similar to The parameters define a region outside the bounds of the array.. |
|  | GenericMarshaller_ColFormatExcFmt | Looks up a localized string similar to Invalid data was encountered for column \"{0}\". Subsequent columns of this row may not contain reliable data.. |
|  | GenericMarshaller_FldFormatExcFmt | Looks up a localized string similar to Invalid data was encountered for field \"{0}\". Further details available in the InnerException. This format or key cannot be sent to data provider.. |
|  | MplxChannel_IOFailure_AggregateFormat | Looks up a localized string similar to {0}, see inner exception for details.. |
|  | MplxChannel_IOFailure_General | Looks up a localized string similar to I/O failure. |
|  | MplxChannel_IOFailure_Send | Looks up a localized string similar to I/O send failure. |
|  | MplxChannel_NegotiateAuth_Exception | Looks up a localized string similar to I/O error occurred during authentication; see inner exception for details.. |
|  | ne_AcceptorResultInvalid | Looks up a localized string similar to An internal error occurred in processing a protocol response. Contact ASNA Support.. |
|  | ne_AcceptSecurityContext | Looks up a localized string similar to Client's security token was rejected by the server, likely due to an Active Directory misconfiguration. Check server logs (Windows Event Viewer, or i5/OS operator message log).. |
|  | ne_AcqCredServerUser | Looks up a localized string similar to System call used to get the DataGate Server process credential failed. Check server's Event Viewer for system and security events.. |
|  | ne_BadTokenInitDecoding | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_CompleteAuthToken | Looks up a localized string similar to System call used to complete authentication failed. If using Active Directory, check connection to key distribution server. Otherwise check Windows workgroup settings (NTLM).. |
|  | ne_CredCacheCursorError | Looks up a localized string similar to Kerberos credential cache access was denied. Server job log may have further details.. |
|  | ne_CredCacheMutexWaitFailure | Looks up a localized string similar to Kerberos credential cache could not be locked for access. Server job log may have further details.. |
|  | ne_CredCacheMutexWaitTimeout | Looks up a localized string similar to Kerberos credential cache access not acquired before timeout period. Check server job logs and system logs.. |
|  | ne_CredCachMutexRelease | Looks up a localized string similar to Kerberos credential cache access release failure. Subsequent access to Kerberos may be blocked on this server.. |
|  | ne_CredInternError | Looks up a localized string similar to Creation of interned credential structure by copying failed.. |
|  | ne_DecodeNtlmLength | Looks up a localized string similar to Invalid protocol message received by the server. This may be caused by an application or network communications error. Check inner exception for details.. |
|  | ne_DecryptMessageFailure | Looks up a localized string similar to System call used to decrypt and/or verify the signature of a secure message failed. Check server Event Viewer logs for errors.. |
|  | ne_DecryptNtlmData | Looks up a localized string similar to System call used to decrypt and verify the signature of a secure message failed. Check server Event Viewer logs for errors.. |
|  | ne_EimConnectFailure | Looks up a localized string similar to System call used to access EIM service failed. Server operator message logs may contain further info.. |
|  | ne_EimConnectInfoQueryFailure | Looks up a localized string similar to System call used to query EIM service connection information failed. Server operator message logs may contain further info.. |
|  | ne_EimCreateHandleFailure | Looks up a localized string similar to System call used to access EIM facility failed. Server operator message logs may contain further info.. |
|  | ne_EimInvalidTargetAssociation | Looks up a localized string similar to No valid target identity type for the logged on user was found. Check server's EIM target registry configuration. . |
|  | ne_EimNoTargetAssociation | Looks up a localized string similar to Target identity not found for the logged on user. Check server's EIM target registry configuration.. |
|  | ne_GetMicFailure | Looks up a localized string similar to System call generating an authentication protocol message failed. Check server logs for errors.. |
|  | ne_GetTargetCredsFromSourceError | Looks up a localized string similar to System call used to resolve a mapping for the authenticated logged on user failed. Check server logs and the server's EIM and LDAP configurations.. |
|  | ne_GetUserNameExFailed | Looks up a localized string similar to System call used to query the authenticated user's impersonated credential failed. Check the server's Event Viewer logs for errors.. |
|  | ne_GssAcquireCredFailed | Looks up a localized string similar to System call used to get the server's host-based service credentials failed. Check server job logs and operator message logs for details.. |
|  | ne_GssAcquireCredForServerFailed | Looks up a localized string similar to The transition from Uninitialized state to WaitingForHandshakeMessage state failed.. |
|  | ne_GssBuildSpnegoTargetFailed | Looks up a localized string similar to System call used to create a protocol server response token failed. Check server job logs and operator message logs for details.. |
|  | ne_GssBuildSpnegoTargetNotParsed | Looks up a localized string similar to System call used to produce a protocol server message token failed. Check server logs for errors.. |
|  | ne_GssKrb5Error | Looks up a localized string similar to The server cannot authenticate due to a Kerberos error. Check job logs and operator message logs for info.. |
|  | ne_GssMechKrb5NotSupported | Looks up a localized string similar to The server supports only Kerberos for single-sign on authentication, but the client did not offer this in the connection negotiation. One cause of this is a misconfigured or misnamed Kerberos service principal.. |
|  | ne_GssReleaseBufferForSendMessage | Looks up a localized string similar to System call used to release security resources failed. Check server logs for errors.. |
|  | ne_GssUnwrapFailed | Looks up a localized string similar to System call used to produce a secure protocol input message failed. Check server logs for errors.. |
|  | ne_GssWrapForSendMessage | Looks up a localized string similar to System call used to produce a secure protocol output message failed. Check server logs for errors.. |
|  | ne_HandshakeErrorMsg | Looks up a localized string similar to Connection authentication was aborted by the client. Check HRESULT error codes in the server logs for more information.. |
|  | ne_HandshakeInProgressSequence | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_HandshakeRequestsUnsupportedNtlm | Looks up a localized string similar to The server does not support the requested downlevel authentication protocol (NTLM). One cause of this is a misconfigured or misnamed Kerberos service principal. Check server's Network Authentication Service configuration, and Active Directory service principal identities. . |
|  | ne_InvalidClientReqMicResponse | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_InvalidHsMessageHeader | Looks up a localized string similar to The server received an invalid protocol message. This may be caused by an application or network communications error.. |
|  | ne_InvalidInitiatorMechlistGenerate | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_Krb5BuildClientPrincipal | Looks up a localized string similar to System call used to build a Kerberos principal token failed. Check server logs, memory, and Network Authentication Service configuration.. |
|  | ne_Krb5ccGenerateNewError | Looks up a localized string similar to System call used to produce a Kerberos object failed. Check server logs, memory, and Network Authentication Service configuration.. |
|  | ne_Krb5CCInitializeError | Looks up a localized string similar to System call used to initialize a Kerberos object failed. Check server logs, memory, and Network Authentication Service configuration.. |
|  | ne_Krb5InitError | Looks up a localized string similar to System call used to initialize the server's Kerberos runtime context failed. Check server job logs and operator message logs for details.. |
|  | ne_Krb5NoDefaultRealm | Looks up a localized string similar to System call used to obtain Kerberos realm failed. Check server logs. Ensure the Network Authentication Service has a correct "default realm" configuration (e.g., the default_realm entry of [libdefaults] section of krb5.conf file). |
|  | ne_Krb5ParseNameError | Looks up a localized string similar to System call used to parse the Service Principal Name provided by the client failed. Check server logs and SPN value.. |
|  | ne_KrbInitialTicketRequest | Looks up a localized string similar to System call used to retrieve a Kerberos service ticket failed. Verify Network Authentication Service identifiers on the server and Active Directory.. |
|  | ne_Mask | Looks up a localized string similar to The server returned an unrecognized error code.. |
|  | ne_MessageFrameLength | Looks up a localized string similar to Invalid protocol message received by the server. This may be caused by an application or network communications error. Check inner exception for details.. |
|  | ne_MessageProtectionFailure | Looks up a localized string similar to System call used to encrypt and/or sign a secure message failed. Check server Event Viewer logs for errors.. |
|  | ne_MissingClientReqMicResponse | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_MissingMechsInHandshakeMessage | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_MissingOrInvalidReqMic | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_NegotiatedImpersonationError | Looks up a localized string similar to The impersonation level required to complete authentication is insufficient. Check the Windows server authentication configuration.. |
|  | ne_NegotiatedProtectionError | Looks up a localized string similar to The protection level required to complete authentication is insufficient. Check the Windows server authentication configuration.. |
|  | ne_NotAuthenticated | Looks up a localized string similar to Connection authentication failed using the logged on user's credentials. If using Active Directory, check connection to domain servers. Otherwise check Windows workgroup settings (NTLM).. |
|  | ne_NotAuthenticatedToSend | Looks up a localized string similar to DataGate message not sent to client because the connection has not been authenticated.. |
|  | ne_OK | Looks up a localized string similar to No Error Detected.. |
|  | ne_ProcessingFinalTokenFailure | Looks up a localized string similar to Connection authentication failed during the negotiation phase. Check server logs and configuration.. |
|  | ne_QueryContextAttributesNegoInfo | Looks up a localized string similar to System call used to query authentication information failed. If using Active Directory, check connection to domain servers. Otherwise check Windows workgroup settings (NTLM).. |
|  | ne_QueryMicrosoftNegotiateSSPI | Looks up a localized string similar to System call used to query the Negotiate SSPI failed. Ensure Negotiate SSPI is enabled on the server, and check server's Event Viewer for system and security events.. |
|  | ne_SocketRecvUnsuccessful | Looks up a localized string similar to System call used to receive a message over the TCP/IP network failed. Check client and server logs.. |
|  | ne_SocketSendUnsuccessful | Looks up a localized string similar to System call used to send a message over the TCP/IP network failed. Check client and server logs.. |
|  | ne_SpnegoParseErrorDefectiveToken | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_SpnegoParseErrorJobLog | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_SpnegoParseErrorOutOfMemory | Looks up a localized string similar to An out-of-memory condition was detected on the server during connection authentication.. |
|  | ne_SpnegoParseIncomplete | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_SpnegoParseInvalidToken | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_SpnegoParseUnknownError | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_TokenRespMechType | Looks up a localized string similar to Protocol violation detected during connection authentication. Check inner exceptions and server logs for all related error codes. Contact ASNA Support if this error persists.. |
|  | ne_TruncatedHandshakeErrorMsg | Looks up a localized string similar to Connection authentication was aborted by the client without a stated reason. This could be a network interruption or more likely a security error. Check client and server logs for information.. |
|  | ne_UnexpectedEndOfStream | Looks up a localized string similar to Client connection ended unexpectedly. This may be caused by an application or network communications error.. |
|  | ne_VerifyNtlmSig | Looks up a localized string similar to System call used to verify the signature of a secure message. Check server Event Viewer logs for errors.. |
|  | NegoExc_Source | Looks up a localized string similar to DataGate Server NegotiateStream Native Implementation. |
|  | NegotateAsyncHelper_DnsHostNotFound | Looks up a localized string similar to Authentication service principal host not found via DNS or hosts table.. |
|  | NegotiateAsyncHelper_EOS | Looks up a localized string similar to Authentication protocol connection closed by remote host.. |
|  | NegotiateAsyncHelper_InvalidKrb5HostIp | Looks up a localized string similar to Invalid IP address notation for authentication service principal name.. |
|  | PackedField_ConversionOverflowFmt | Looks up a localized string similar to System.Decimal value ({0}) out of bounds for Packed({1},{2}) field.. |
|  | PackedField_InvalidDataFmt | Looks up a localized string similar to Invalid System.Decimal data in Packed field (record offset {0}).. |
|  | PackedField_InvalidTransFmt | Looks up a localized string similar to Invalid stripped translation of System.Decimal value ({0}) to ({1}).. |
|  | ParmTypeRep_AttrMissingFmt | Looks up a localized string similar to Expected value for attribute '{0}'.. |
|  | ParmTypeRep_DtfHmsNotSupported | Looks up a localized string similar to Invalid date/time format specified (HMS is not supported).. |
|  | ParmTypeRep_DtfIsoNotSupported | Looks up a localized string similar to Invalid date/time format specified (ISO is not supported).. |
|  | ParmTypeRep_InvByteSize | Looks up a localized string similar to Invalid byte size specified (expected 1).. |
|  | ParmTypeRep_InvFloatSize | Looks up a localized string similar to Invalid floating point size specified (expected 4 or 8).. |
|  | ParmTypeRep_InvIntSize | Looks up a localized string similar to Invalid integer size specified (expected 2 or 4).. |
|  | ParmTypeRep_ParmCircularity | Looks up a localized string similar to The parameter description is a parent of the current parameter.. |
|  | ParmTypeRep_ParmDupNameFmt | Looks up a localized string similar to The current parameter already has a member named '{0}'.. |
|  | PrintFile_ExpectedActiveRow | Looks up a localized string similar to The AdgDataSet does not contain an active row.. |
|  | PrintFile_FeodFailure | Looks up a localized string similar to Print file FEOD operation failed (see inner exception for details).. |
|  | PrintFile_FeodFileNotOpen | Looks up a localized string similar to Print file not opened.. |
|  | PrintFile_InvalidOperation | Looks up a localized string similar to This operation is invalid for .NET print files.. |
|  | PrintFile_ResetFailure | Looks up a localized string similar to Print file failed Reset procedure. See InnerException for detail.. |
|  | PrintingProps_RendererElementReadOnly | Looks up a localized string similar to Renderer element is read-only.. |
|  | PrintingProps_RendererSettingReadOnly | Looks up a localized string similar to Renderer setting's value element is read-only.. |
|  | PrintingProps_SectionLocked | Looks up a localized string similar to PrintingProps section cannot be modified.. |
|  | ProgParm_ArgExcDontCareDirectionNone | Looks up a localized string similar to DataTypes.DontCare may only be specified with DataDirection.None.. |
|  | RpcSync_Reentrancy | Looks up a localized string similar to Reentrancy detected.. |
|  | SecureStringSafeBuffer_UpdateNotAllowed | Looks up a localized string similar to Cannot update a read-only SecureString. Either pass a SecureString instance that is not marked read-only, or change the value of the update parameter to 'false'.. |
|  | SocketAsyncHelper_EOS | Looks up a localized string similar to TCP connection closed by remote host.. |
|  | SourceFactory_ExtConfigException | Looks up a localized string similar to DataGate client extension loading failed, possibly due to misconfiguration.. |
|  | SourceFactory_PlatformNotSupported | Looks up a localized string similar to This version of DataGate does not support the specified database source's Platform Attribute property.. |
|  | SqlBulkWriteFileBase_AdoExcRecCountFmt | Looks up a localized string similar to {1}Record #{0}.. |
|  | SqlBulkWriteFileBase_AdoNet | Looks up a localized string similar to ADO.NET. |
|  | SqlBulkWriteFileBase_BackgroundExcFmt | Looks up a localized string similar to An exception, "{0}", occurred in a worker task. See InnerException for details.. |
|  | SqlBulkWriteFileBase_DateTimeMismatch | Looks up a localized string similar to Field type does not correspond to a column.. |
|  | SqlBulkWriteFileBase_ErrorFmt | Looks up a localized string similar to {0}: Bulk copy terminated in batch #{1} (records {2} through {3}).. |
|  | SqlBulkWriteFileBase_ErrRecNumFmt | Looks up a localized string similar to Error writing record #{0}.. |
|  | SqlBulkWriteFileBase_FormatExcFmt | Looks up a localized string similar to Invalid data was encountered for field "{0}". Further details available in the InnerException. This format or key cannot be sent to data provider.. |
|  | SqlBulkWriteFileBase_InvalidFormatFmt | Looks up a localized string similar to Invalid format element name '{0}'.. |
|  | SqlFileAttr_InvBinColDfltFmt | Looks up a localized string similar to Invalid default binary value '{0}' for column '{1}'.. |
|  | SqlFileAttr_InvDtColDfltFmt | Looks up a localized string similar to Invalid default date or time value '{0}' for column '{1}'.. |
|  | SqlFileObject_MaxMembersOutOfRange | Looks up a localized string similar to Allowed Max Members values are -1 (*NOMAX), 0 (*DEFAULT), or any number in the range [1..32767].. |
|  | SqlFileObject_UdfAggregate | Looks up a localized string similar to User defined types errors occurred.. |
|  | SqlObjectName_InvalidQuotedId | Looks up a localized string similar to Quoted identifiers found but without a '.' separator.. |
|  | SqlTimeConverter_TimeValueOverflow | Looks up a localized string similar to Time value '{0}' is outside of expected range.. |
|  | SslAsyncHelper_AuthComplete_NoEncryption | Looks up a localized string similar to Authentication completed, but encryption is unavailable for the session.. |
|  | SslAsyncHelper_AuthComplete_NotAuth | Looks up a localized string similar to Authentication completed, but the session failed validation.. |
|  | SslAsyncHelper_EOS | Looks up a localized string similar to SSL connection closed by remote host.. |
|  | SslAsyncHelper_InvalidIP | Looks up a localized string similar to Connected server host did not resolve to a valid IP address (details in inner exception).. |
|  | SslAsyncHelper_IpParseFailureFmt | Looks up a localized string similar to Cannot parse '{0}' as a valid server host IP address.. |
|  | SslExc_Dialog_Banner | Looks up a localized string similar to The DataGate server's identity cannot be verified for reasons stated below. To abort this connection and correct potential security problems, select the Cancel option.. |
|  | SslExc_Dialog_Button3 | Looks up a localized string similar to View Certificate.... |
|  | SslExc_Dialog_Cancel | Looks up a localized string similar to Cancel. |
|  | SslExc_Dialog_Proceed | Looks up a localized string similar to Proceed. |
|  | SslExc_Dialog_Title | Looks up a localized string similar to DataGate Network Security Alert. |
|  | SslExc_PromptFormat | Looks up a localized string similar to To ignore the above exceptions and initiate the possibly insecure connection anyway, enter "{0}" ({1}/{2}?):. |
|  | StructureType_ArgExcNoMembers | Looks up a localized string similar to Structure with no members specified.. |
|  | UserPasswordCredential_ReadOnly | Looks up a localized string similar to Cannot modify user/password credential object because it has been marked as read-only.. |
|  | UserPasswordCredential_StarDomainPassword | Looks up a localized string similar to Cannot set password for *DOMAIN credential.. |
|  | ZonedField_ConversionOverflowFmt | Looks up a localized string similar to System.Decimal value ({0}) out of bounds for Zoned({1},{2}) field.. |