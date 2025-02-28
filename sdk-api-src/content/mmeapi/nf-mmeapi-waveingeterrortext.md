---
UID: NF:mmeapi.waveInGetErrorText
title: waveInGetErrorText function (mmeapi.h)
description: The waveInGetErrorText function retrieves a textual description of the error identified by the given error number.
old-location: multimedia\waveingeterrortext.htm
tech.root: Multimedia
ms.assetid: 49d24beb-795a-4399-b230-c65cc16337dc
ms.date: 12/05/2018
ms.keywords: _win32_waveInGetErrorText, mmeapi/waveInGetErrorText, multimedia.waveingeterrortext, waveInGetErrorText, waveInGetErrorText function [Windows Multimedia]
ms.topic: function
f1_keywords:
- mmeapi/waveInGetErrorText
dev_langs:
- c++
req.header: mmeapi.h
req.include-header: Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Winmm.dll
api_name:
- waveInGetErrorText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# waveInGetErrorText function


## -description



The <b>waveInGetErrorText</b> function retrieves a textual description of the error identified by the given error number.




## -parameters




### -param mmrError

Error number.


### -param pszText

Pointer to the buffer to be filled with the textual error description.


### -param cchText

Size, in characters, of the buffer pointed to by <i>pszText</i>.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADERRNUM</b></dt>
</dl>
</td>
<td width="60%">
Specified error number is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No device driver is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate or lock memory.

</td>
</tr>
</table>
 




## -remarks



If the textual error description is longer than the specified buffer, the description is truncated. The returned error string is always null-terminated. If <i>cchText</i> is zero, nothing is copied and the function returns zero. All error descriptions are less than MAXERRORLENGTH characters long.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>
 

 

