---
Description: Compile an effect.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: ID3DXEffectCompiler::CompileEffect method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXEffectCompiler::CompileEffect method

Compile an effect.

## Syntax


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## Parameters

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Compile options identified by various flags. The Direct3D 10 HLSL compiler is now the default. See [D3DXSHADER Flags](d3dxshader-flags.md) for details.

</dd> <dt>

*ppEffect* \[out, retval\]
</dt> <dd>

Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer containing the compiled effect. For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[out, retval\]
</dt> <dd>

Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer containing at least the first compile error message that occurred. This includes effect compiler errors and high-level language compile errors. For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is S\_OK.

If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.

If the method fails, the return value will be E\_FAIL.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 



