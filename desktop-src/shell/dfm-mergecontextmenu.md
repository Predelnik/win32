﻿---
Description: 'Allows the callback to add items to the menu.'
title: 'DFM\_MERGECONTEXTMENU message'
---

# DFM\_MERGECONTEXTMENU message

Allows the callback to add items to the menu.


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## Parameters

<dl> <dt>

*pqcminfo* \[in\]
</dt> <dd>

A pointer to a [**QCMINFO**](qcminfo-str.md) structure containing the information used in the merge.

</dd> <dt>

*uFlags* \[in\]
</dt> <dd>

Flags specifying how the context menu can be changed. This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](icontextmenu-querycontextmenu.md).

</dd> </dl>

## Remarks

If items are added to the context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).

This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented. There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](cdeffoldermenu-create2.md), [**SHCreateDefaultContextMenu**](shcreatedefaultcontextmenu.md).

[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback. Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.

## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                          |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 



