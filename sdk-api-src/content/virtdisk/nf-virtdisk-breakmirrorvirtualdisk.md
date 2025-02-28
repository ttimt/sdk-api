---
UID: NF:virtdisk.BreakMirrorVirtualDisk
title: BreakMirrorVirtualDisk function (virtdisk.h)
description: Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.
old-location: vhd\breakmirrorvirtualdisk.htm
tech.root: VStor
ms.assetid: bf70ee43-9fba-4856-a1bc-85eec61f5763
ms.date: 12/05/2018
ms.keywords: BreakMirrorVirtualDisk, BreakMirrorVirtualDisk function [VHD], vdssys/BreakMirrorVirtualDisk, vhd.breakmirrorvirtualdisk, virtdisk/BreakMirrorVirtualDisk
ms.topic: function
f1_keywords:
- virtdisk/BreakMirrorVirtualDisk
dev_langs:
- c++
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- VirtDisk.dll
api_name:
- BreakMirrorVirtualDisk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BreakMirrorVirtualDisk function


## -description


Breaks a previously initiated mirror operation and sets the mirror to be the active virtual 
    disk.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open mirrored virtual disk. For information on how to open a virtual disk, see the 
      <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function. For information on how to 
      mirror a virtual disk, see the <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a> 
      function.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a>



<a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>
 

 

