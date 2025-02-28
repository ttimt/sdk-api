---
UID: NF:strmif.IConfigAviMux.SetOutputCompatibilityIndex
title: IConfigAviMux::SetOutputCompatibilityIndex (strmif.h)
description: The SetOutputCompatibilityIndex method sets the AVI index format.
old-location: dshow\iconfigavimux_setoutputcompatibilityindex.htm
tech.root: DirectShow
ms.assetid: 3b9793e6-e5f4-432f-95f6-62053b955348
ms.date: 12/05/2018
ms.keywords: IConfigAviMux interface [DirectShow],SetOutputCompatibilityIndex method, IConfigAviMux.SetOutputCompatibilityIndex, IConfigAviMux::SetOutputCompatibilityIndex, IConfigAviMuxSetOutputCompatibilityIndex, SetOutputCompatibilityIndex, SetOutputCompatibilityIndex method [DirectShow], SetOutputCompatibilityIndex method [DirectShow],IConfigAviMux interface, dshow.iconfigavimux_setoutputcompatibilityindex, strmif/IConfigAviMux::SetOutputCompatibilityIndex
ms.topic: method
f1_keywords:
- strmif/IConfigAviMux.SetOutputCompatibilityIndex
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IConfigAviMux.SetOutputCompatibilityIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigAviMux::SetOutputCompatibilityIndex


## -description



The <code>SetOutputCompatibilityIndex</code> method sets the AVI index format.




## -parameters




### -param fOldIndex [in]

Specifies one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Create an AVI 1.0 index, as well as an AVI 2.0 index.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Create an AVI 2.0 index, but not an AVI 1.0 index.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



The AVI Mux filter always creates an AVI 2.0 index ('indx' format). If the value given in <i>fOldIndex</i> is <b>TRUE</b>, the AVI Mux also creates an AVI 1.0 index ('idx1' format), for backward compatibility with Video for Windows.

The AVI 2.0 index format allows for larger files, incremental growth of files, and minimized disk seeks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iconfigavimux">IConfigAviMux Interface</a>
 

 

