---
UID: NF:vds.IVdsVolume.GetPack
title: IVdsVolume::GetPack (vds.h)
description: Retrieves the pack to which the volume is a member.
old-location: base\ivdsvolume_getpack.htm
tech.root: VDS
ms.assetid: 8719c4a4-a7d6-4329-a601-5c88de18f53d
ms.date: 12/05/2018
ms.keywords: GetPack, GetPack method [VDS], GetPack method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],GetPack method, IVdsVolume.GetPack, IVdsVolume::GetPack, base.ivdsvolume_getpack, vds/IVdsVolume::GetPack
ms.topic: method
f1_keywords:
- vds/IVdsVolume.GetPack
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsVolume.GetPack
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolume::GetPack


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the pack to which the volume is a member.


## -parameters




### -param ppPack [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a> interface pointer. The caller must release the interface.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>
 

 

