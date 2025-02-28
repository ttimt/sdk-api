---
UID: NF:interlockedapi.InterlockedPushListSListEx
title: InterlockedPushListSListEx function (interlockedapi.h)
description: Inserts a singly-linked list at the front of another singly linked list. Access to the lists is synchronized on a multiprocessor system. This version of the method does not use the __fastcall calling convention.
old-location: base\interlockedpushlistslistex.htm
tech.root: Sync
ms.assetid: f4f334c6-fda8-4c5f-9177-b672c8aed6b3
ms.date: 12/05/2018
ms.keywords: InterlockedPushListSListEx, InterlockedPushListSListEx function, base.interlockedpushlistslistex, interlockedapi/InterlockedPushListSListEx
ms.topic: function
f1_keywords:
- interlockedapi/InterlockedPushListSListEx
dev_langs:
- c++
req.header: interlockedapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-interlocked-l1-2-0.dll
- KernelBase.dll
- MinKernelBase.dll
api_name:
- InterlockedPushListSListEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedPushListSListEx function


## -description


Inserts a singly-linked list at the front of another singly linked list. Access to the lists is synchronized on a multiprocessor system. This version of the method does not use the <a href="https://docs.microsoft.com/previous-versions/6xa169sk(v=vs.85)">__fastcall</a> calling convention.


## -parameters




### -param ListHead [in, out]

Pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. The list specified by the <i>List</i> and <i>ListEnd</i> parameters is inserted at the front of this list.


### -param List [in, out]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-_list_entry">SLIST_ENTRY</a> structure that represents the first item in the  list to be inserted. 


### -param ListEnd [in, out]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-_list_entry">SLIST_ENTRY</a> structure that represents the last item in the  list to be inserted. 


### -param Count [in]

The number of items in the list to be inserted.


## -returns



The return value is the previous first item in the list specified by the <i>ListHead</i> parameter. If the list was previously empty, the return value is <b>NULL</b>.




## -remarks



All list items must be aligned on a <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary; otherwise, this function will behave unpredictably. See <b>_aligned_malloc</b>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist">InterlockedFlushSList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a>



<a href="/windows/desktop/api/winnt/ns-winnt-_list_entry">SLIST_ENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>
 

 

