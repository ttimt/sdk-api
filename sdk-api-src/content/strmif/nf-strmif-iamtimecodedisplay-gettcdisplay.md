---
UID: NF:strmif.IAMTimecodeDisplay.GetTCDisplay
title: IAMTimecodeDisplay::GetTCDisplay (strmif.h)
description: The GetTCDisplay method retrieves current settings of the timecode character generator output.
old-location: dshow\iamtimecodedisplay_gettcdisplay.htm
tech.root: DirectShow
ms.assetid: 3da33500-1b1d-4818-b69b-74f302614349
ms.date: 12/05/2018
ms.keywords: GetTCDisplay, GetTCDisplay method [DirectShow], GetTCDisplay method [DirectShow],IAMTimecodeDisplay interface, IAMTimecodeDisplay interface [DirectShow],GetTCDisplay method, IAMTimecodeDisplay.GetTCDisplay, IAMTimecodeDisplay::GetTCDisplay, IAMTimecodeDisplayGetTCDisplay, dshow.iamtimecodedisplay_gettcdisplay, strmif/IAMTimecodeDisplay::GetTCDisplay
ms.topic: method
f1_keywords:
- strmif/IAMTimecodeDisplay.GetTCDisplay
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
- IAMTimecodeDisplay.GetTCDisplay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeDisplay::GetTCDisplay


## -description



The <code>GetTCDisplay</code> method retrieves current settings of the timecode character generator output.




## -parameters




### -param Param [in]

Timecode display characteristic. Specify one of the following items you want to get settings for.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCD_BORDER</td>
<td>White border for black characters, black border for white characters.</td>
</tr>
<tr>
<td>ED_TCD_INTENSITY</td>
<td>Intensity (brightness) of characters.</td>
</tr>
<tr>
<td>ED_TCD_INVERT</td>
<td>Black characters on white background or white characters on black background.</td>
</tr>
<tr>
<td>ED_TCD_POSITION</td>
<td>Position of characters.</td>
</tr>
<tr>
<td>ED_TCD_SIZE</td>
<td>Size of characters.</td>
</tr>
<tr>
<td>ED_TCD_SOURCE</td>
<td>Source of display's data.</td>
</tr>
<tr>
<td>ED_TCD_TRANSPARENCY</td>
<td>Transparency of characters.</td>
</tr>
</table>
 


### -param pValue [out]

Pointer to the current setting of the parameter specified in <i>Param</i>. This parameter retrieves one of the following values.

If ED_TCD_SOURCE specified in <i>Param</i>, will return one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG</td>
<td>Timecode generator</td>
</tr>
<tr>
<td>ED_TCR</td>
<td>Timecode reader</td>
</tr>
</table>
 

If ED_TCD_SIZE specified in <i>Param</i>, will return one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_LARGE</td>
<td>Large</td>
</tr>
<tr>
<td>ED_MED</td>
<td>Medium</td>
</tr>
<tr>
<td>ED_SMALL</td>
<td>Small</td>
</tr>
</table>
 

If ED_TCD_POSITION specified in <i>Param</i>, will return one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_BOTTOM</td>
<td>Bottom</td>
</tr>
<tr>
<td>ED_MIDDLE</td>
<td>Middle</td>
</tr>
<tr>
<td>ED_TOP</td>
<td>Top</td>
</tr>
</table>
 

in combination with one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_CENTER</td>
<td>Center</td>
</tr>
<tr>
<td>ED_LEFT</td>
<td>Left</td>
</tr>
<tr>
<td>ED_RIGHT</td>
<td>Right</td>
</tr>
</table>
 

If ED_TCD_INTENSITY specified in <i>Param</i>, will return one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_HIGH</td>
<td>High</td>
</tr>
<tr>
<td>ED_LOW</td>
<td>Low</td>
</tr>
</table>
 

If ED_TCD_TRANSPARENCY is specified in <i>Param</i>, will return a value from 0 to 4, 0 being completely opaque.

If ED_TCD_INVERT is specified in <i>Param</i>, will return one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OAFALSE</td>
<td>Black characters on white background</td>
</tr>
<tr>
<td>OATRUE</td>
<td>White characters on black background</td>
</tr>
</table>
 

If ED_TCD_BORDER specified in <i>Param</i>, will return one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OAFALSE</td>
<td>Black characters for white border</td>
</tr>
<tr>
<td>OATRUE</td>
<td>White border for black characters</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtimecodedisplay">IAMTimecodeDisplay Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-settcdisplay">IAMTimecodeDisplay::SetTCDisplay</a>
 

 

