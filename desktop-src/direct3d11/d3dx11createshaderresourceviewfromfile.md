---
title: D3DX11CreateShaderResourceViewFromFile function
description: Note The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows�8 and is not supported for Windows Store apps.�Note Instead of using this function, we recommend that you use these DirectXTK library (runtime), CreateXXXTextureFromFile (where XXX is DDS or WIC)DirectXTex library (tools), LoadFromXXXFile (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then CreateShaderResourceView�Create a shader-resource view from a file.
ms.assetid: 'c6a23503-f511-49dc-a0dc-19932cf8f313'
keywords: ["D3DX11CreateShaderResourceViewFromFile function Direct3D 11"]
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
---

# D3DX11CreateShaderResourceViewFromFile function

> [!Note]  
> The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows�8 and is not supported for Windows Store apps.

�

> [!Note]  
> Instead of using this function, we recommend that you use these:
>
> -   [DirectXTK](http://go.microsoft.com/fwlink/p/?linkid=248929) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)
> -   [DirectXTex](http://go.microsoft.com/fwlink/p/?linkid=248926) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**

�

Create a shader-resource view from a file.

## Syntax


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_��ID3D11Device ������������*pDevice,
  _In_��LPCTSTR �����������������pSrcFile,
  _In_��D3DX11_IMAGE_LOAD_INFO ��*pLoadInfo,
  _In_��ID3DX11ThreadPump �������*pPump,
  _Out_�ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_�HRESULT �����������������*pHResult
);
```



## Parameters

<dl> <dt>

*pDevice* \[in\]
</dt> <dd>

Type: **[**ID3D11Device**](id3d11device.md)\***

A pointer to the device (see [**ID3D11Device**](id3d11device.md)) that will use the resource.

</dd> <dt>

*pSrcFile* \[in\]
</dt> <dd>

Type: **[**LPCTSTR**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Name of the file that contains the shader-resource view. If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR. Otherwise, the data type resolves to LPCSTR.

</dd> <dt>

*pLoadInfo* \[in\]
</dt> <dd>

Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***

Optional. Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.

</dd> <dt>

*pPump* \[in\]
</dt> <dd>

Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). If **NULL** is specified, this function will behave synchronously and will not return until it is finished.

</dd> <dt>

*ppShaderResourceView* \[out\]
</dt> <dd>

Type: **[**ID3D11ShaderResourceView**](id3d11shaderresourceview.md)\*\***

Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](id3d11shaderresourceview.md)).

</dd> <dt>

*pHResult* \[out\]
</dt> <dd>

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)\***

A pointer to the return value. May be **NULL**. If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

## Remarks

For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## See also

<dl> <dt>

[D3DX Functions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

�

�




