---
UID: NF:gpmgmt.IGPMGPO.GetWMIFilter
title: IGPMGPO::GetWMIFilter (gpmgmt.h)
description: Retrieves the GPMWMIFilter object linked to the Group Policy object (GPO).
old-location: gpmc\igpmgpo_getwmifilter.htm
tech.root: gpmc
ms.assetid: eca1dffb-1e92-42a1-b950-c6c6c88bd064
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],GetWMIFilter method, GetWMIFilter, GetWMIFilter method [GPMC], GetWMIFilter method [GPMC],GPMGPO class, GetWMIFilter method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GetWMIFilter method, IGPMGPO.GetWMIFilter, IGPMGPO::GetWMIFilter, _win32_igpmgpo_getwmifilter, gpmc.igpmgpo_getwmifilter, gpmgmt/IGPMGPO::GetWMIFilter
ms.topic: method
f1_keywords:
- gpmgmt/IGPMGPO.GetWMIFilter
dev_langs:
- c++
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gpmgmt.dll
api_name:
- IGPMGPO.GetWMIFilter
- GPMGPO.GetWMIFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMGPO::GetWMIFilter


## -description


Retrieves the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object linked to the Group Policy object (GPO).


## -parameters




### -param ppIGPMWMIFilter [out]

Address of a pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns S_FALSE if no WMI filter is linked to the GPO. Returns a failure code if an error occurs.

<h3>JScript</h3>
If the GPO is linked to a WMI filter, the method returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object. If the GPO is not linked to a WMI filter, the method returns a null reference.

<h3>VB</h3>
If the GPO is linked to a WMI filter, the method returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object. If the GPO is not linked to a WMI filter, the method returns a null reference.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
 

 

