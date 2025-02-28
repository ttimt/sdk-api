---
UID: NF:wincrypt.PFXExportCertStoreEx
title: PFXExportCertStoreEx function (wincrypt.h)
description: Exports the certificates and, if available, their associated private keys from the referenced certificate store.
old-location: security\pfxexportcertstoreex.htm
tech.root: SecCrypto
ms.assetid: e8bd54b1-946f-4c65-8a86-96f0dbec07ff
ms.date: 12/05/2018
ms.keywords: EXPORT_PRIVATE_KEYS, PFXExportCertStoreEx, PFXExportCertStoreEx function [Security], PKCS12_INCLUDE_EXTENDED_PROPERTIES, PKCS12_PROTECT_TO_DOMAIN_SIDS, REPORT_NOT_ABLE_TO_EXPORT_PRIVATE_KEY, REPORT_NO_PRIVATE_KEY, _crypto2_pfxexportcertstoreex, security.pfxexportcertstoreex, wincrypt/PFXExportCertStoreEx
ms.topic: function
f1_keywords:
- wincrypt/PFXExportCertStoreEx
dev_langs:
- c++
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- PFXExportCertStoreEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFXExportCertStoreEx function


## -description


The <b>PFXExportCertStoreEx</b> function exports the certificates and, if available, their associated private keys from the referenced certificate store. This function replaces the older 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstore">PfxExportCertStore</a> function. It should be used for its enhanced private key security. The PFX BLOB created by this function is protected by a password.


## -parameters




### -param hStore [in]

Handle of the certificate store containing the certificates to be exported.


### -param pPFX [in, out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure to contain the PFX packet with the exported certificates and keys. If <i>pPFX</i>-&gt;<i>pbData</i> is <b>NULL</b>, the function calculates the number of bytes needed for the encoded BLOB and returns this in <i>pPFX</i>-&gt;<i>cbData</i>. When the function is called with <i>pPFX</i>-&gt;<i>pbData</i> pointing to an allocated buffer of the needed size, the function copies the encoded bytes into the buffer and updates <i>pPFX</i>-&gt;<i>cbData</i> with the encode byte length.


### -param szPassword [in]

String password used to encrypt and verify the PFX packet. When you have finished using the password, clear the password from memory by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://docs.microsoft.com/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.


### -param pvPara [in]

This parameter must be <b>NULL</b> if the <i>dwFlags</i> parameter does not contain <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b>. Prior to Windows 8 and Windows Server 2012, therefore, this parameter must be <b>NULL</b>.

Beginning with Windows 8 and Windows Server 2012, if the <i>dwFlags</i> parameter contains <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b>, you can set the <i>pvPara</i> parameter to point to an <b>NCRYPT_DESCRIPTOR_HANDLE</b> value to identify which Active Directory principal the PFX password will be protected to inside of the PFX BLOB. Currently, the password can be protected to an Active Directory user, computer, or group. For more information about protection descriptors, see <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>.


### -param dwFlags [in]

Flag values can be set to any combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXPORT_PRIVATE_KEYS"></a><a id="export_private_keys"></a><dl>
<dt><b>EXPORT_PRIVATE_KEYS</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Private keys are exported as well as the certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="REPORT_NO_PRIVATE_KEY"></a><a id="report_no_private_key"></a><dl>
<dt><b>REPORT_NO_PRIVATE_KEY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
If a certificate is encountered that has no associated private key, the function returns FALSE with the last error set to either CRYPT_E_NOT_FOUND or NTE_NO_KEY.

</td>
</tr>
<tr>
<td width="40%"><a id="REPORT_NOT_ABLE_TO_EXPORT_PRIVATE_KEY"></a><a id="report_not_able_to_export_private_key"></a><dl>
<dt><b>REPORT_NOT_ABLE_TO_EXPORT_PRIVATE_KEY</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
If a certificate is encountered that has a non-exportable private key, the function returns FALSE and the last error set to NTE_BAD_KEY, NTE_BAD_KEY_STATE, or NTE_PERM.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_INCLUDE_EXTENDED_PROPERTIES"></a><a id="pkcs12_include_extended_properties"></a><dl>
<dt><b>PKCS12_INCLUDE_EXTENDED_PROPERTIES</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Export all extended
properties on the certificate.

 


<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_PROTECT_TO_DOMAIN_SIDS"></a><a id="pkcs12_protect_to_domain_sids"></a><dl>
<dt><b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The PFX BLOB contains an embedded password that will be protected to the Active Directory (AD) protection descriptor pointed to by the <i>pvPara</i> parameter. If the <i>szPassword</i> parameter is not  <b>NULL</b> or empty, the specified password is protected. If, however,  the <i>szPassword</i> parameter is <b>NULL</b> or an empty string, a random forty (40)  character password is created and protected.


<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore">PFXImportCertStore</a> uses the specified protection descriptor to decrypt the embedded password, whether specified by the user or randomly generated, and then uses the password to decrypt the PFX BLOB.

<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
</table>
 


## -returns



Returns <b>TRUE</b> (nonzero) if the function succeeds, and <b>FALSE</b> (zero) if the function fails. For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Beginning with Windows 8 and Windows Server 2012, you can protect the PFX password to an Active Directory user, computer, or group. If you choose to do so but do not create a password, a temporary password will be randomly selected. The password is encrypted by using the Active Directory principal and then embedded in the PFX BLOB. For more information, see the <i>pvPara</i> parameter and the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstore">PFXExportCertStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore">PFXImportCertStore</a>
 

 

