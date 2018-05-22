---
title: WM\_NCPOINTERUPDATE message
description: Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.
ms.assetid: '3bdc37da-227c-4be1-bf0b-99704caa1322'
keywords: ["WM_NCPOINTERUPDATE message Input Messages and Notifications"]
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
---

# WM\_NCPOINTERUPDATE message

Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window. While the pointer is hovering, the message targets whichever window the pointer happens to be over. While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.

If a window has captured this pointer, this message is not posted. Instead, a [**WM\_POINTERUPDATE**](wm-pointerupdate.md) is posted to the window that has captured this pointer.

> \[!Important\]  
> Desktop apps should be DPI aware. If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization. DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off). For more information, see [Writing High-DPI Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/dd464660).

�


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

Contains the pointer identifier and additional information. Use the following macros to retrieve this information.

[**GET\_POINTERID\_WPARAM**](get-pointerid-wparam.md)(wParam): pointer identifier

[**HIWORD**](https://msdn.microsoft.com/library/windows/desktop/ms632657)(wParam): hit-test value returned from processing the [**WM\_NCHITTEST**](https://msdn.microsoft.com/library/windows/desktop/ms645618) message.

</dd> <dt>

*lParam* 
</dt> <dd>

Contains the point location of the pointer.

> [!Note]  
> Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area. Whenever possible, an application should use the complete pointer area information instead of the point location.

�

Use the following macros to retrieve the physical screen coordinates of the point.

-   [**GET\_X\_LPARAM**](https://msdn.microsoft.com/library/windows/desktop/ms632654)(lParam): the x (horizontal point) coordinate.
-   [**GET\_Y\_LPARAM**](https://msdn.microsoft.com/library/windows/desktop/ms632655)(lParam): the y (vertical point) coordinate.

</dd> </dl>

## Return value

If an application processes this message, it should return zero.

If the application does not process this message, it should call [**DefWindowProc**](https://msdn.microsoft.com/library/windows/desktop/ms633572).

## Remarks

If the application does not process this message, [**DefWindowProc**](https://msdn.microsoft.com/library/windows/desktop/ms633572) may perform one or more system actions depending on the hit-test result included in the message. Typically, applications should not need to handle this message.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�8 \[desktop apps only\]<br/>                                                               |
| Minimum supported server<br/> | Windows Server�2012 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

�

�




