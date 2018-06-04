---
title: WM\_POINTERACTIVATE message
description: Sent to an inactive window when a primary pointer generates a WM\_POINTERDOWN over the window.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTIVATE message Input Messages and Notifications
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WM\_POINTERACTIVATE message

Sent to an inactive window when a primary pointer generates a [**WM\_POINTERDOWN**](wm-pointerdown.md) over the window. As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window. Applications can respond to this message to specify whether they wish to be activated.

A window receives this message through its [**WindowProc**](https://msdn.microsoft.com/library/windows/desktop/ms633573) function.


```C++
#define WM_POINTERACTIVATE             0x024B
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

Contains the pointer identifier and additional information. Use the following macros to retrieve this information.

[**GET\_POINTERID\_WPARAM**](/windows/desktop/api/Winuser/nf-winuser-get_pointerid_wparam)(wParam): pointer identifier

[**HIWORD**](https://msdn.microsoft.com/library/windows/desktop/ms632657)(wParam): hit-test value returned from processing the [**WM\_NCHITTEST**](https://msdn.microsoft.com/library/windows/desktop/ms645618) message.

</dd> <dt>

*lParam* 
</dt> <dd>

Contains the handle to the top-level window of the window being activated.

</dd> </dl>

## Return value

If an application processes this message, it should return one of the values described in the Remarks section.

If the application does not process this message, it should call [**DefWindowProc**](https://msdn.microsoft.com/library/windows/desktop/ms633572).

## Remarks

An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:

-   PA\_ACTIVATE
-   PA\_NOACTIVATE

It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM\_POINTERACTIVATE** message represents is available to applications only for the first of those pointers. Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.

If the application does not handle this message, [**DefWindowProc**](https://msdn.microsoft.com/library/windows/desktop/ms633572) passes the message to the parent window.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                                               |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

 

 




