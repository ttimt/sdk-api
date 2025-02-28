---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_SCOPE_INFO
title: D3D10_SHADER_DEBUG_SCOPE_INFO (d3d10_1shader.h)
description: Contains scope data that maps variable names to debug variables.
old-location: direct3d10\d3d10_shader_debug_scope_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_scope_info.htm
ms.date: 12/05/2018
ms.keywords: 98b3a0e8-be0d-c4db-defc-df94817adf46, D3D10_SHADER_DEBUG_SCOPE_INFO, D3D10_SHADER_DEBUG_SCOPE_INFO structure [Direct3D 10], d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_INFO, direct3d10.d3d10_shader_debug_scope_info
ms.topic: struct
f1_keywords:
- d3d10_1shader/D3D10_SHADER_DEBUG_SCOPE_INFO
dev_langs:
- c++
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- d3d10_1shader.h
api_name:
- D3D10_SHADER_DEBUG_SCOPE_INFO
targetos: Windows
req.typenames: D3D10_SHADER_DEBUG_SCOPE_INFO
req.redist: 
ms.custom: 19H1
---

# D3D10_SHADER_DEBUG_SCOPE_INFO structure


## -description


Contains scope data that maps variable names to debug variables.


## -struct-fields




### -field ScopeType

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/d3d10_1shader/ne-d3d10_1shader-d3d10_shader_debug_scopetype">D3D10_SHADER_DEBUG_SCOPETYPE</a></b>

Specifies the scope type.


### -field Name

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the name of scope in the strings list.


### -field uNameLen

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the string pointed to by <b>Name</b>.


### -field uVariables

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of variables.


### -field VariableData

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset an array of UINT values with <b>uVariables</b> members contianing the scope variable list.


## -remarks



The <b>D3D10_SHADER_DEBUG_SCOPE_INFO</b> structure is used with the <a href="https://docs.microsoft.com/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
 

 

