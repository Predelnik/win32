---
title: DisableDiskDrives method of the Win32\_TSGatewayConnectionAuthorizationPolicy class
description: Sets the DiskDrivesDisabled property.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 'bdc4a923-bda7-464a-95eb-95231374ac93'
ms.prod: 'windows-server-dev'
ms.technology: 'remote-desktop-services'
ms.tgt_platform: multiple
keywords: ["DisableDiskDrives method Remote Desktop Services", "DisableDiskDrives method Remote Desktop Services , Win32_TSGatewayConnectionAuthorizationPolicy class", "Win32_TSGatewayConnectionAuthorizationPolicy class Remote Desktop Services , DisableDiskDrives method"]
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableDiskDrives
api_location:
- AagWmi.dll
api_type:
- COM
---

# DisableDiskDrives method of the Win32\_TSGatewayConnectionAuthorizationPolicy class

Sets the **DiskDrivesDisabled** property. If the **DeviceRedirectionType** property has a value of "2", the **DiskDrivesDisabled** property controls redirection of the client disk drives for sessions that are established through the Remote Desktop Gateway (RD�Gateway) server.

## Syntax


```mof
uint32 DisableDiskDrives(
  [in]�boolean Disabled
);
```



## Parameters

<dl> <dt>

*Disabled* \[in\]
</dt> <dd>

New value for the **DiskDrivesDisabled** property.

</dd> </dl>

## Return value

If the method succeeds, it returns zero. If the method is unsuccessful, it returns a nonzero value. For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).

## Remarks

You must be a member of the Administrators group to call this method.

Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes. MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK). They are installed on the server when you add the associated role by using the Server Manager. For more information about MOF files, see [Managed Object Format (MOF)](https://msdn.microsoft.com/library/aa823192).

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                |
| Minimum supported server<br/> | Windows Server�2008<br/>                                                           |
| Namespace<br/>                | Root\\CIMv2\\TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## See also

<dl> <dt>

[**Win32\_TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

�

�




