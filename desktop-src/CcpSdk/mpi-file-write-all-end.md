---
Description: 'TBD.'
audience: developer
author: 'REDMOND\\danlep'
manager: 'REDMOND\\timlt'
ms.assetid: 'd9ec9d1a-e525-4cf7-8fb6-62234efaba92'
ms.prod: 'windows-server-dev'
ms.technology: 'compute-cluster-pack'
ms.tgt_platform: multiple
title: 'MPI\_File\_write\_all\_end function'
---

# MPI\_File\_write\_all\_end function

TBD

## Syntax


```C++
int MPIAPI MPI_File_write_all_end(
  ������MPI_File ��file,
  _In_��void ������*buf,
  _Out_�MPI_Status *status
);
```



## Parameters

<dl> <dt>

*file* 
</dt> <dd>

TBD

</dd> <dt>

*buf* \[in\]
</dt> <dd>

TBD

</dd> <dt>

*status* \[out\]
</dt> <dd>

TBD

</dd> </dl>

## Return value

TBD

## Fortran

``` syntax
MPI_FILE_WRITE_ALL_END(FH, BUF, STATUS, IERROR)
    <type> BUF(*)
    INTEGER FH, STATUS(MPI_STATUS_SIZE), IERROR
```

## Requirements



|                    |                                                                                                                                                                                          |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Product<br/> | HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities<br/> |
| Header<br/>  | <dl> <dt>Mpi.h; </dt> <dt>Mpif.h</dt> </dl>                                           |
| Library<br/> | <dl> <dt>Msmpi.lib</dt> </dl>                                                                                                     |
| DLL<br/>     | <dl> <dt>Msmpi.dll</dt> </dl>                                                                                                     |



## See also

<dl> <dt>

[MPI File Functions](mpi-file-functions.md)
</dt> </dl>

�

�



