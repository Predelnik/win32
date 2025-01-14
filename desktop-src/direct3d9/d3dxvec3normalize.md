---
Description: Returns the normalized version of a 3D vector.
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: D3DXVec3Normalize function
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- D3DXVec3Normalize
api_type: 
- LibDef
api_location: 
- d3dx9.lib
- d3dx9.dll
---

# D3DXVec3Normalize function

Returns the normalized version of a 3D vector.

## Syntax


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## Parameters

<dl> <dt>

*pOut* \[in, out\]
</dt> <dd>

Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***

Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.

</dd> <dt>

*pV* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***

Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.

</dd> </dl>

## Return value

Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***

Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.

## Remarks

The return value for this function is the same value returned in the *pOut* parameter. In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Math Functions](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




