---
title: D3DX11CompileFromMemory function
description: Note The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows�8 and is not supported for Windows Store apps.�Note Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the D3DCompile API.�Compile a shader or an effect that is loaded in memory.
ms.assetid: '3396560f-f411-4c66-9f22-03c0050c74b0'
keywords: ["D3DX11CompileFromMemory function Direct3D 11"]
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
---

# D3DX11CompileFromMemory function

> [!Note]  
> The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows�8 and is not supported for Windows Store apps.

�

> [!Note]  
> Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](https://msdn.microsoft.com/library/windows/desktop/dd607324) API.

�

Compile a shader or an effect that is loaded in memory.

## Syntax


```C++
HRESULT D3DX11CompileFromMemory(
  _In_��������LPCSTR ������������pSrcData,
  _In_��������SIZE_T ������������SrcDataLen,
  _In_��������LPCSTR ������������pFileName,
  _In_��const D3D10_SHADER_MACRO *pDefines,
  _In_��������LPD3D10INCLUDE ����pInclude,
  _In_��������LPCSTR ������������pFunctionName,
  _In_��������LPCSTR ������������pProfile,
  _In_��������UINT ��������������Flags1,
  _In_��������UINT ��������������Flags2,
  _In_��������ID3DX11ThreadPump �*pPump,
  _Out_�������ID3D10Blob ��������**ppShader,
  _Out_�������ID3D10Blob ��������**ppErrorMsgs,
  _Out_�������HRESULT �����������*pHResult
);
```



## Parameters

<dl> <dt>

*pSrcData* \[in\]
</dt> <dd>

Type: **[**LPCSTR**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Pointer to the shader in memory.

</dd> <dt>

*SrcDataLen* \[in\]
</dt> <dd>

Type: **[**SIZE\_T**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Size of the shader in memory.

</dd> <dt>

*pFileName* \[in\]
</dt> <dd>

Type: **[**LPCSTR**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

The name of the file that contains the shader code.

</dd> <dt>

*pDefines* \[in\]
</dt> <dd>

Type: **const [**D3D10\_SHADER\_MACRO**](https://msdn.microsoft.com/library/windows/desktop/bb172436)\***

Optional. Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](https://msdn.microsoft.com/library/windows/desktop/bb172436)). The last structure in the array serves as a terminator and must have all members set to 0. If not used, set *pDefines* to **NULL**.

</dd> <dt>

*pInclude* \[in\]
</dt> <dd>

Type: **[**LPD3D10INCLUDE**](https://msdn.microsoft.com/library/windows/desktop/bb173775)**

Optional. Pointer to an interface for handling include files. Setting this to **NULL** will cause a compile error if a shader contains a \#include.

</dd> <dt>

*pFunctionName* \[in\]
</dt> <dd>

Type: **[**LPCSTR**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Name of the shader-entry point function where shader execution begins. When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.

</dd> <dt>

*pProfile* \[in\]
</dt> <dd>

Type: **[**LPCSTR**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5. The profile can also be for effect type (for example, fx\_4\_1).

</dd> <dt>

*Flags1* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Shader [**compile flags**](https://msdn.microsoft.com/library/windows/desktop/gg615083).

</dd> <dt>

*Flags2* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

Effect [**compile flags**](https://msdn.microsoft.com/library/windows/desktop/gg615084). When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.

</dd> <dt>

*pPump* \[in\]
</dt> <dd>

Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***

A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Use **NULL** to specify that this function should not return until it is completed.

</dd> <dt>

*ppShader* \[out\]
</dt> <dd>

Type: **[**ID3D10Blob**](https://msdn.microsoft.com/library/windows/desktop/bb173507)\*\***

A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.

</dd> <dt>

*ppErrorMsgs* \[out\]
</dt> <dd>

Type: **[**ID3D10Blob**](https://msdn.microsoft.com/library/windows/desktop/bb173507)\*\***

A pointer to memory which contains a listing of errors and warnings that occurred during compilation. These errors and warnings are identical to the debug output from a debugger.

</dd> <dt>

*pHResult* \[out\]
</dt> <dd>

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)\***

A pointer to the return value. May be **NULL**. If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter. For more information about this situation, see Remarks.

## Remarks

For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](https://msdn.microsoft.com/library/windows/desktop/dd607324).

You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter. Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to. To create a shader from complied shader code, you call one of the following [**ID3D11Device**](id3d11device.md) interface methods:

-   [**CreateComputeShader**](id3d11device-createcomputeshader.md)
-   [**CreateDomainShader**](id3d11device-createdomainshader.md)
-   [**CreateGeometryShader**](id3d11device-creategeometryshader.md)
-   [**CreateGeometryShaderWithStreamOutput**](id3d11device-creategeometryshaderwithstreamoutput.md)
-   [**CreateHullShader**](id3d11device-createhullshader.md)
-   [**CreatePixelShader**](id3d11device-createpixelshader.md)
-   [**CreateVertexShader**](id3d11device-createvertexshader.md)

In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## See also

<dl> <dt>

[D3DX Functions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

�

�




