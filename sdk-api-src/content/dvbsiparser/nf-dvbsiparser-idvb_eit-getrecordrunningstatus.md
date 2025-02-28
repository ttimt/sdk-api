---
UID: NF:dvbsiparser.IDVB_EIT.GetRecordRunningStatus
title: IDVB_EIT::GetRecordRunningStatus (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit_getrecordrunningstatus.htm
tech.root: mstv
ms.assetid: fc5d4bc7-4d56-453f-90ed-6187f55ea464
ms.date: 12/05/2018
ms.keywords: GetRecordRunningStatus, GetRecordRunningStatus method [Microsoft TV Technologies], GetRecordRunningStatus method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetRecordRunningStatus method, IDVB_EIT.GetRecordRunningStatus, IDVB_EIT::GetRecordRunningStatus, IDVB_EITGetRecordRunningStatus, dvbsiparser/IDVB_EIT::GetRecordRunningStatus, mstv.idvb_eit_getrecordrunningstatus
ms.topic: method
f1_keywords:
- dvbsiparser/IDVB_EIT.GetRecordRunningStatus
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
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
- COM
api_location:
- dvbsiparser.h
api_name:
- IDVB_EIT.GetRecordRunningStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_EIT::GetRecordRunningStatus


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRunningStatus</b> method returns the running status of a particular event in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number for the event, indexed from zero. Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getcountofrecords">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.


### -param pbVal [out]

Pointer to a variable that receives the running_status field. See the Remarks section in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordrunningstatus">IDVB_RST::GetRecordRunningStatus</a> method for more information.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>
 

 

