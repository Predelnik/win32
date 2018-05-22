---
title: ID3DX11EffectMatrixVariable SetMatrix method
description: Set a floating-point matrix.
ms.assetid: '91c69bc0-c8c6-4232-8c70-801ac8ddbcda'
keywords: ["SetMatrix method Direct3D 11", "SetMatrix method Direct3D 11 , ID3DX11EffectMatrixVariable interface", "ID3DX11EffectMatrixVariable interface Direct3D 11 , SetMatrix method"]
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
---

# ID3DX11EffectMatrixVariable::SetMatrix method

Set a floating-point matrix.

## Syntax


```C++
HRESULT SetMatrix(
  �float *pData
);
```



## Parameters

<dl> <dt>

*pData* 
</dt> <dd>

Type: **float\***

A pointer to the first element in the matrix.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

## Remarks

> [!Note]  
> The DirectX SDK does not supply any compiled binaries for effects. You must use Effects 11 source to build your effects-type application. For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).

�

## Requirements



|                    |                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Library<br/> | <dl> <dt>N/A (An Effects 11 library is available online as shared source.)</dt> </dl> |



## See also

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

�

�




