---
Description: Evaluates an expression in debug and retail builds. In debug builds, displays a diagnostic message if the expression is FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE\_ASSERT macro
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# EXECUTE\_ASSERT macro

Evaluates an expression in debug and retail builds. In debug builds, displays a diagnostic message if the expression is **FALSE**.

## Syntax


```C++
void EXECUTE_ASSERT(
    cond
);
```



## Parameters

<dl> <dt>

*cond* 
</dt> <dd>

Expression to evaluate.

</dd> </dl>

## Return value

This macro does not return a value.

## Remarks

Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds. In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number. The user can ignore the assertion, enter the debugger, or quit the application.

## Requirements



|                   |                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## See also

<dl> <dt>

[Assert and Breakpoint Macros](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 



