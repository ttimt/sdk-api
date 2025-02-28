---
UID: NS:wlanapi._WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
title: WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
description: A structure that represents a device service notification.
ms.date: 12/18/2019
ms.topic: language-reference
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wlanapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: WLAN_DEVICE_SERVICE_NOTIFICATION_DATA, *PWLAN_DEVICE_SERVICE_NOTIFICATION_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
f1_keywords:
 - wlanapi/_WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
 - wlanapi/WLAN_DEVICE_SERVICE_NOTIFICATION_DATA
dev_langs:
 - c++
---

## -description

A structure that represents a device service notification.

## -struct-fields

### -field DeviceService

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The **GUID** identifying the device service for this notification.

### -field dwOpCode

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The opcode that identifies the operation under the device service for this notification.

### -field dwDataSize

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The size, in bytes, of the *DataBlob* member. The maximum value of *dwDataSize* may be restricted by the type of data that is stored in the **WLAN_DEVICE_SERVICE_NOTIFICATION_DATA** structure.

### -field DataBlob

Type: **[BYTE](/windows/win32/api/guiddef/ns-guiddef-guid)\[1\]**

A pointer to an array containing **BYTES**s, representing the data blob. This is the data that is received from the independent hardware vendor (IHV) driver, and is passed on to the client as an unformatted byte array blob.

## -remarks

## -see-also