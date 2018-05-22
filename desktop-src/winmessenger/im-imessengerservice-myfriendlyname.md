---
title: IMessengerService MyFriendlyName property
description: Retrieves the local user's friendly name that corresponds to the selected service.
ms.assetid: 'ac83ec10-e7d4-45cf-a577-a232bea53917'
keywords: ["MyFriendlyName property Windows Messenger", "MyFriendlyName property Windows Messenger , IMessengerService interface", "IMessengerService interface Windows Messenger , MyFriendlyName property"]
topic_type:
- apiref
api_name:
- IMessengerService.MyFriendlyName
- IMessengerService.get_MyFriendlyName
api_location:
- Msgsc.dll
api_type:
- COM
---

# IMessengerService::MyFriendlyName property

\[**MyFriendlyName** is no longer available for use as of Windows�Vista. See [Windows Messenger](im-messenger-entry.md) for more information.\]

Retrieves the local user's friendly name that corresponds to the selected service.

This property is read-only.

## Syntax


```C++
HRESULT get_MyFriendlyName(
  [out, retval]�BSTR *pbstrName
);
```



## Property value

Pointer to a **BSTR** containing the friendly name for the local user of this service.

## Error codes

Returns one of the following values.



| Name                                                                                                  | Meaning                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S\_OK</dt> </dl>                      | Success. <br/>                               |
| <dl> <dt>RPC\_X\_NULL\_REF\_POINTER</dt> </dl> | *pbstrName* is a **NULL** pointer.<br/>      |
| <dl> <dt>E\_FAIL</dt> </dl>                    | *pbstrName* returned a **NULL** string.<br/> |
| <dl> <dt>E\_OUTOFMEMORY</dt> </dl>             | String comparison failed.<br/>               |
| <dl> <dt>MSGR\_E\_NOT\_LOGGED\_ON</dt> </dl>   | This service is offline.<br/>                |



## Remarks

The following table lists error codes returned by this method.



| Error Code               | Meaning                                                  |
|--------------------------|----------------------------------------------------------|
| 0x80004005               | *pbstrName* returned a **NULL** string.                  |
| 0x8007000E               | String comparison failed.                                |
| MSGR\_E\_NOT\_LOGGED\_ON | The local user is not logged in to the selected service. |



�

For a table of MSGR\_E\_\* constants, see [**MSGRConstants**](im-msgrconstants.md).

> [!Note]  
> This property is not available for scripting languages.

�

## Examples

The following Visual Basic example shows the use of this method.


```VB
Public WithEvents MsgrUIA As MessengerAPI.Messenger
Public MsgrServices As MessengerAPI.IMessengerServices

Private Sub btnServicesCount_Click()
    On Error Resume Next
    MsgBox("Services Count= " & CStr(MsgrServices.Count))
    ErrorTrap ("MsgrServices.Count")    'Error handling routine
End Sub
```



## Requirements



|                                  |                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------|
| End of client support<br/> | Windows�XP<br/>                                                                 |
| End of server support<br/> | Windows Server�2003<br/>                                                        |
| Header<br/>                | <dl> <dt>Msgrua.h</dt> </dl>   |
| IDL<br/>                   | <dl> <dt>Msgrua.idl</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Msgsc.dll</dt> </dl>  |



## See also

<dl> <dt>

[**IMessengerService**](im-imessengerservice.md)
</dt> <dt>

[**MySigninName**](im-imessengerservice-mysigninname.md)
</dt> <dt>

[**MyStatus**](im-imessengerservice-mystatus.md)
</dt> </dl>

�

�




