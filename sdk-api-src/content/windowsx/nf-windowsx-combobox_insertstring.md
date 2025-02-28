---
UID: NF:windowsx.ComboBox_InsertString
title: ComboBox_InsertString macro (windowsx.h)
description: Adds a string to a list in a combo box at the specified location. You can use this macro or send the CB_INSERTSTRING message explicitly.
old-location: controls\ComboBox_InsertString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_insertstring.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_InsertString, ComboBox_InsertString macro [Windows Controls], _win32_ComboBox_InsertString, _win32_ComboBox_InsertString_cpp, controls.ComboBox_InsertString, controls._win32_ComboBox_InsertString, windowsx/ComboBox_InsertString
ms.topic: macro
f1_keywords:
- windowsx/ComboBox_InsertString
dev_langs:
- c++
req.header: windowsx.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Windowsx.h
api_name:
- ComboBox_InsertString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_InsertString macro


## -description


Adds a string to a list in a combo box at the specified location. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index at which to insert the string, or –1 to add it to the end of the list. 


### -param lpsz

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The string to add.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a>.
	



