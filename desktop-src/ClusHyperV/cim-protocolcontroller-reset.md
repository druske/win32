---
title: Reset method of the CIM\_ProtocolController class
description: Resets the logical device.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: '29a2d8ca-7f54-4975-bc5c-cda950fbaed3'
ms.prod: 'windows-server-dev'
ms.technology:
- 'failover-cluster-hyperv'
- 'windows-management-instrumentation'
ms.tgt_platform: multiple
keywords: ["Reset method", "Reset method, CIM_ProtocolController class", "CIM_ProtocolController class, Reset method"]
topic_type:
- apiref
api_name:
- CIM_ProtocolController.Reset
api_location:
- VMMS.exe
api_type:
- COM
---

# Reset method of the CIM\_ProtocolController class

Resets the logical device.

## Syntax


```mof
uint32 Reset();
```



## Parameters

This method has no parameters.

## Return value

The possible return values are:

<dl> <dt>


</dt> <dd>

0

The operation completed successfully.

</dd> <dt>


</dt> <dd>

1

The operation was not completed because it is not supported.

</dd> <dt>


</dt> <dd>

2

The operation is not supported when the device is in the current state.

</dd> <dt>


</dt> <dd>

3�...

The operation was not completed because an error occurred.

</dd> </dl>

## Requirements



|                                     |                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                              |
| Minimum supported server<br/> | Windows Server�2016<br/>                                                                         |
| Namespace<br/>                | Root\\HyperVCluster\\v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsHyperVCluster.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>VMMS.exe</dt> </dl>                    |



## See also

<dl> <dt>

[**CIM\_ProtocolController**](cim-protocolcontroller.md)
</dt> </dl>

�

�




