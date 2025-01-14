---
title: IVMVirtualMachine RemoveNetworkAdapter method
description: Removes a network interface from the virtual machine.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- RemoveNetworkAdapter method Virtual PC
- RemoveNetworkAdapter method Virtual PC , IVMVirtualMachine interface
- IVMVirtualMachine interface Virtual PC , RemoveNetworkAdapter method
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
---

# IVMVirtualMachine::RemoveNetworkAdapter method

\[Windows Virtual PC is no longer available for use as of Windows 8. Instead, use the [Hyper-V WMI provider (V2)](https://docs.microsoft.com/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Removes a network interface from the virtual machine.

## Syntax


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## Parameters

<dl> <dt>

*networkAdapter* \[in\]
</dt> <dd>

An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.

</dd> </dl>

## Return value

This method can return one of these values.



| Return code/value                                                                                                                                                            | Description                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S\_OK**</dt> <dt>0</dt> </dl>                                  | The operation was successful.<br/>                       |
| <dl> <dt>**E\_POINTER**</dt> <dt>0x80004003</dt> </dl>                    | The parameter is **NULL**.<br/>                          |
| <dl> <dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | The configuration is unknown.<br/>                       |
| <dl> <dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt> </dl> | The virtual machine is in a running or saved state.<br/> |
| <dl> <dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | An unexpected error has occurred.<br/>                   |



 

## Remarks

You can only remove an existing network interface from a virtual machine that is stopped.

## Requirements



|                                     |                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                                    |
| Minimum supported server<br/> | None supported<br/>                                                                     |
| End of client support<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## See also

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

 





