---
UID: NF:pdh.PdhIsRealTimeQuery
title: PdhIsRealTimeQuery function (pdh.h)
description: Determines if the specified query is a real-time query.
old-location: perf\pdhisrealtimequery.htm
tech.root: perfctrs
ms.assetid: 4f6b2d8d-3a0f-4346-8b8e-a7aea11fbc40
ms.date: 12/05/2018
ms.keywords: PdhIsRealTimeQuery, PdhIsRealTimeQuery function [Perf], _win32_pdhisrealtimequery, base.pdhisrealtimequery, pdh/PdhIsRealTimeQuery, perf.pdhisrealtimequery
ms.topic: function
f1_keywords:
- pdh/PdhIsRealTimeQuery
dev_langs:
- c++
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Pdh.dll
api_name:
- PdhIsRealTimeQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhIsRealTimeQuery function


## -description


Determines if the specified query is a real-time query.
		


## -parameters




### -param hQuery [in]

Handle to the query. The 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function returns this handle.


## -returns



If the query is a real-time query, the return value is <b>TRUE</b>.
						

If the query is not a real-time query, the return value is <b>FALSE</b>.




## -remarks



The term <i>real-time</i> as used in the description of this function does not imply the standard meaning of the term <i>real-time</i>. Instead, it describes the collection of performance data from a source providing current information (for example, the registry or a WMI provider) rather than from a log file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhselectdatasourcea">PdhSelectDataSource</a>
 

 

