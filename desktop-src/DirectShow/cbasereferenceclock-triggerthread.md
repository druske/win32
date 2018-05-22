---
Description: 'The TriggerThread method wakes up the worker thread that handles scheduling.'
ms.assetid: '296a6b59-fc52-4f5e-8a19-6b534a253a6e'
title: 'CBaseReferenceClock.TriggerThread method'
---

# CBaseReferenceClock.TriggerThread method

The `TriggerThread` method wakes up the worker thread that handles scheduling.

## Syntax


```C++
void TriggerThread();
```



## Parameters

This method has no parameters.

## Return value

This method does not return a value.

## Remarks

The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times. The derived class can call `TriggerThread` to wake up the thread.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBaseReferenceClock Class**](cbasereferenceclock.md)
</dt> </dl>

�

�



