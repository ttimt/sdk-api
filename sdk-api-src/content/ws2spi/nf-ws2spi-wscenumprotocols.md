---
UID: NF:ws2spi.WSCEnumProtocols
title: WSCEnumProtocols function (ws2spi.h)
description: The WSCEnumProtocols function retrieves information about available transport protocols.
old-location: winsock\wscenumprotocols_2.htm
tech.root: WinSock
ms.assetid: c2e5332f-3327-4624-96b4-8e321795961d
ms.date: 12/05/2018
ms.keywords: WSCEnumProtocols, WSCEnumProtocols function [Winsock], _win32_wscenumprotocols_2, winsock.wscenumprotocols_2, ws2spi/WSCEnumProtocols
ms.topic: function
f1_keywords:
- ws2spi/WSCEnumProtocols
dev_langs:
- c++
req.header: ws2spi.h
req.include-header: 
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ws2_32.dll
api_name:
- WSCEnumProtocols
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSCEnumProtocols function


## -description


The 
**WSCEnumProtocols** function retrieves information about available transport protocols.


## -parameters




### -param lpiProtocols [in]

A **NULL**-terminated array of <i>iProtocol</i> values. This parameter is optional; if <i>lpiProtocols</i> is NULL, information on all available protocols is returned. Otherwise, information is retrieved only for those protocols listed in the array.


### -param lpProtocolBuffer [out]

A pointer to a buffer that is filled with 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infow">WSAPROTOCOL_INFOW</a> structures.


### -param lpdwBufferLength [in, out]

On input, size of the <i>lpProtocolBuffer</i> buffer passed to 
**WSCEnumProtocols**, in bytes. On output, the minimum buffer size, in bytes, that can be passed to 
**WSCEnumProtocols** to retrieve all the requested information.


### -param lpErrno [out]

A pointer to the error code.


## -returns



If no error occurs, 
**WSCEnumProtocols** returns the number of protocols to be reported on. Otherwise, a value of SOCKET_ERROR is returned and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
One of more of the arguments is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
Buffer length was too small to receive all the relevant 
[WSAProtocol_Info](https://docs.microsoft.com/en-us/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures and associated information. Pass in a buffer at least as large as the value returned in <i>lpdwBufferLength</i>.

</td>
</tr>
</table>
 




## -remarks



The **WSCEnumProtocols** function is used to discover information about the collection of transport protocols installed on the local computer. This function differs from its API counterpart (<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>) in that 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infow">WSAPROTOCOL_INFOW</a> structures for all installed protocols are returned. This includes protocols that the service provider has set the **PFL_HIDDEN** flag in the **dwProviderFlags** member of the **WSAPROTOCOL_INFOW** structure to indicate to the Ws2_32.dll that this protocol should not be returned in the result buffer generated by **WSAEnumProtocols** function.  In addition, the **WSCEnumProtocols** also returns data for **WSAPROTOCOL_INFOW** structures that have a chain length of zero ( a dummy LSP provider).   The **WSAEnumProtocols** only returns information on base protocols and protocol chains that lack the **PFL_HIDDEN** flag  and don't have a protocol chain length of zero. 

<div class="alert">**Note**  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="https://docs.microsoft.com/windows/desktop/FWP/windows-filtering-platform-start-page">Windows Filtering Platform</a>.</div>
<div> </div>
The <i>lpiProtocols</i> parameter can be used as a filter to constrain the amount of information provided. Typically, a null pointer is supplied so the function will return information on all available transport protocols.

A 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infow">WSAPROTOCOL_INFOW</a> structure is provided in the buffer pointed to by <i>lpProtocolBuffer</i> for each requested protocol. If the supplied buffer is not large enough (as indicated by the input value of <i>lpdwBufferLength</i>), the value pointed to by <i>lpdwBufferLength</i> will be updated to indicate the required buffer size. The Windows Sockets SPI client should then obtain a large enough buffer and call this function again. The 
**WSCEnumProtocols** function cannot enumerate over multiple calls; the passed-in buffer must be large enough to hold all expected entries in order for the function to succeed. This reduces the complexity of the function and should not pose a problem because the number of protocols loaded on a local computer is typically small.

The order in which the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infow">WSAPROTOCOL_INFOW</a> structures appear in the buffer coincides with the order in which the protocol entries were registered by the service provider with the WS2_32.dll, or with any subsequent reordering that may have occurred through the Windows Sockets applet supplied for establishing default transport providers.


#### Examples

The following example demonstrates the use of the **WSCEnumProtocols** function to retrieve an array of <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infow">WSAPROTOCOL_INFOW</a> structures for protocols installed on the local computer.


```cpp
#ifndef UNICODE
#define UNICODE 1
#endif

#include <winsock2.h>
#include <ws2tcpip.h>
#include <ws2spi.h>
#include <objbase.h>
#include <stdio.h>

// Link with ws2_32.lib and ole32.lib
#pragma comment (lib, "Ws2_32.lib")
#pragma comment (lib, "ole32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))
// Note: could also use malloc() and free()

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult = 0;

    INT iNuminfo = 0;

    int i;

    // Allocate a 16K buffer to retrieve all the protocol providers
    DWORD dwBufferLen = 16384;
    LPWSAPROTOCOL_INFOW lpProtocolInfo = NULL;
    int iErrno = 0;

    // variables needed for converting provider GUID to a string
    int iRet = 0;
    WCHAR GuidString[40] = { 0 };

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }

    lpProtocolInfo = (LPWSAPROTOCOL_INFOW) MALLOC(dwBufferLen);
    if (lpProtocolInfo == NULL) {
        wprintf(L"Memory allocation for providers buffer failed\n");
        WSACleanup();
        return 1;
    }

    iNuminfo = WSCEnumProtocols(NULL, lpProtocolInfo, &dwBufferLen, &iErrno);
    if (iNuminfo == SOCKET_ERROR) {
        if (iErrno != WSAENOBUFS) {
            wprintf(L"WSCEnumProtocols failed with error: %d\n", iErrno);
            if (lpProtocolInfo) {
                FREE(lpProtocolInfo);
                lpProtocolInfo = NULL;
            }
            WSACleanup();
            return 1;
        } else {
            wprintf(L"WSCEnumProtocols failed with error: WSAENOBUFS (%d)\n",
                    iErrno);
            wprintf(L"  Increasing buffer size to %d\n\n", dwBufferLen);
            if (lpProtocolInfo) {
                FREE(lpProtocolInfo);
                lpProtocolInfo = NULL;
            }
            lpProtocolInfo = (LPWSAPROTOCOL_INFOW) MALLOC(dwBufferLen);
            if (lpProtocolInfo == NULL) {
                wprintf(L"Memory allocation increase for buffer failed\n");
                WSACleanup();
                return 1;
            }
            iNuminfo =
                WSCEnumProtocols(NULL, lpProtocolInfo, &dwBufferLen, &iErrno);
            if (iNuminfo == SOCKET_ERROR) {
                wprintf(L"WSCEnumProtocols failed with error: %d\n", iErrno);
                if (lpProtocolInfo) {
                    FREE(lpProtocolInfo);
                    lpProtocolInfo = NULL;
                }
                WSACleanup();
                return 1;
            }

        }
    }

    wprintf(L"WSCEnumProtocols succeeded with protocol count = %d\n\n",
            iNuminfo);
    for (i = 0; i < iNuminfo; i++) {
        wprintf(L"Winsock Catalog Provider Entry #%d\n", i);
        wprintf
            (L"----------------------------------------------------------\n");
        wprintf(L"Entry type:\t\t\t ");
        if (lpProtocolInfo[i].ProtocolChain.ChainLen == 1)
            wprintf(L"Base Service Provider\n");
        else
            wprintf(L"Layered Chain Entry\n");

        wprintf(L"Protocol:\t\t\t %ws\n", lpProtocolInfo[i].szProtocol);

        iRet =
            StringFromGUID2(lpProtocolInfo[i].ProviderId,
                            (LPOLESTR) & GuidString, 39);
        if (iRet == 0)
            wprintf(L"StringFromGUID2 failed\n");
        else
            wprintf(L"Provider ID:\t\t\t %ws\n", GuidString);

        wprintf(L"Catalog Entry ID:\t\t %u\n",
                lpProtocolInfo[i].dwCatalogEntryId);

        wprintf(L"Version:\t\t\t %d\n", lpProtocolInfo[i].iVersion);

        wprintf(L"Address Family:\t\t\t %d\n",
                lpProtocolInfo[i].iAddressFamily);
        wprintf(L"Max Socket Address Length:\t %d\n",
                lpProtocolInfo[i].iMaxSockAddr);
        wprintf(L"Min Socket Address Length:\t %d\n",
                lpProtocolInfo[i].iMinSockAddr);

        wprintf(L"Socket Type:\t\t\t %d\n", lpProtocolInfo[i].iSocketType);
        wprintf(L"Socket Protocol:\t\t %d\n", lpProtocolInfo[i].iProtocol);
        wprintf(L"Socket Protocol Max Offset:\t %d\n",
                lpProtocolInfo[i].iProtocolMaxOffset);

        wprintf(L"Network Byte Order:\t\t %d\n",
                lpProtocolInfo[i].iNetworkByteOrder);
        wprintf(L"Security Scheme:\t\t %d\n",
                lpProtocolInfo[i].iSecurityScheme);
        wprintf(L"Max Message Size:\t\t %u\n", lpProtocolInfo[i].dwMessageSize);

        wprintf(L"ServiceFlags1:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags1);
        wprintf(L"ServiceFlags2:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags2);
        wprintf(L"ServiceFlags3:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags3);
        wprintf(L"ServiceFlags4:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwServiceFlags4);
        wprintf(L"ProviderFlags:\t\t\t 0x%x\n",
                lpProtocolInfo[i].dwProviderFlags);

        wprintf(L"Protocol Chain length:\t\t %d\n",
                lpProtocolInfo[i].ProtocolChain.ChainLen);

        wprintf(L"\n");
    }

    if (lpProtocolInfo) {
        FREE(lpProtocolInfo);
        lpProtocolInfo = NULL;
    }
    WSACleanup();

    return 0;
}


```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infow">WSAPROTOCOL_INFOW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wscenumprotocols32">WSCEnumProtocols32</a>
 

 

