---
UID: NN:evr.IMFVideoRenderer
title: IMFVideoRenderer (evr.h)
description: Sets a new mixer or presenter for the Enhanced Video Renderer (EVR).
old-location: mf\imfvideorenderer.htm
tech.root: medfound
ms.assetid: 70596630-5131-460f-9cb3-adcea201c3b2
ms.date: 12/05/2018
ms.keywords: 70596630-5131-460f-9cb3-adcea201c3b2, IMFVideoRenderer, IMFVideoRenderer interface [Media Foundation], IMFVideoRenderer interface [Media Foundation],described, evr/IMFVideoRenderer, mf.imfvideorenderer
ms.topic: interface
f1_keywords:
- evr/IMFVideoRenderer
dev_langs:
- c++
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoRenderer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoRenderer interface


## -description


Sets a new mixer or presenter for the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR).

Both the EVR media sink and the DirectShow EVR filter implement this interface. To get a pointer to the interface, call <b>QueryInterface</b> on the media sink or the filter. Do not use <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a> to get a pointer to this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoRenderer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer">InitializeRenderer</a>
</td>
<td align="left" width="63%">
Sets a new mixer or presenter for the enhanced video renderer (EVR).

</td>
</tr>
</table> 


## -remarks



The EVR activation object returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate">MFCreateVideoRendererActivate</a> function does not expose this interface. Instead, the activation object supports attributes that specify a custom mixer or presenter. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer-attributes">Enhanced Video Renderer Attributes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

