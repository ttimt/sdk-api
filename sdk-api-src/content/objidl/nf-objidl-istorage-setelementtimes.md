---
UID: NF:objidl.IStorage.SetElementTimes
title: IStorage::SetElementTimes (objidl.h)
description: The SetElementTimes method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.
old-location: stg\istorage_setelementtimes.htm
tech.root: Stg
ms.assetid: f6a1fba4-0444-4de3-a838-2d339878fe24
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],SetElementTimes method, IStorage.SetElementTimes, IStorage::SetElementTimes, SetElementTimes, SetElementTimes method [Structured Storage], SetElementTimes method [Structured Storage],IStorage interface, _stg_istorage_setelementtimes, objidl/IStorage::SetElementTimes, stg.istorage_setelementtimes
ms.topic: method
f1_keywords:
- objidl/IStorage.SetElementTimes
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IStorage.SetElementTimes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage::SetElementTimes


## -description


The <b>SetElementTimes</b>  method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.


## -parameters




### -param pwcsName [in]

The name of the storage object element whose times are to be modified. If <b>NULL</b>, the time is set on the root storage rather than one of its elements.


### -param pctime [in]

Either the new creation time for the element or <b>NULL</b> if the creation time is not to be modified.


### -param patime [in]

Either the new access time for the element or <b>NULL</b> if the access time is not to be modified.


### -param pmtime [in]

Either the new modification time for the element or <b>NULL</b> if the modification time is not to be modified.


## -returns



This method can return one of these values.




## -remarks



<b>SetElementTimes</b>  sets time statistics for the specified storage element within this storage object.

Not all file systems support all the time values. This method sets those times that are supported and ignores the rest. Each time-value parameter can be <b>NULL</b>; indicating that no modification should occur.

Call the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method to retrieve these time values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>
 

 

