---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.GetValue
title: IEnumCERTVIEWATTRIBUTE::GetValue (certview.h)
description: Retrieves the value of the current attribute in the attribute-enumeration sequence.
old-location: security\ienumcertviewattribute_getvalue.htm
tech.root: SecCrypto
ms.assetid: a03a6da4-d286-487e-a292-8a02626325a8
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Security], GetValue method [Security],IEnumCERTVIEWATTRIBUTE interface, IEnumCERTVIEWATTRIBUTE interface [Security],GetValue method, IEnumCERTVIEWATTRIBUTE.GetValue, IEnumCERTVIEWATTRIBUTE::GetValue, _certsrv_ienumcertviewattribute_getvalue, certview/IEnumCERTVIEWATTRIBUTE::GetValue, security.ienumcertviewattribute_getvalue
ms.topic: method
f1_keywords:
- certview/IEnumCERTVIEWATTRIBUTE.GetValue
dev_langs:
- c++
req.header: certview.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Certadm.dll
api_name:
- IEnumCERTVIEWATTRIBUTE.GetValue
- IEnumCERTVIEWATTRIBUTE.GetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumCERTVIEWATTRIBUTE::GetValue


## -description


The <b>GetValue</b> method retrieves the value of the current attribute in the attribute-enumeration sequence.


## -parameters




### -param pstrOut [out]

A pointer to a <b>BSTR</b> type that contains the value of the attribute.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pstrOut</i> is set to the value of the current attribute.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that represents the value of the current attribute.




## -remarks



This method is used to retrieve the data in the attribute currently referenced by the 
attribute-enumeration sequence.

If the attribute-enumeration sequence is not referencing a valid attribute, <b>GetValue</b> will fail. Use 
one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-reset">IEnumCERTVIEWATTRIBUTE::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a>: Moves to the next attribute in the enumeration sequence.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-skip">IEnumCERTVIEWATTRIBUTE::Skip</a>: Skips a specified number of attributes.</li>
</ul>

#### Examples


```cpp
BSTR    bstrAttribValue = NULL;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
hr = pEnumAttr->GetValue(&bstrAttribValue);
if (S_OK != hr)
    printf("Failed call to GetValue - %x\n", hr);
else
    printf("Attribute value is %ws\n",bstrAttribValue);

// free memory when done
if (NULL != bstrAttribValue)
    SysFreeString(bstrAttribValue);
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-getname">IEnumCERTVIEWATTRIBUTE::GetName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-next">IEnumCERTVIEWATTRIBUTE::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-reset">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certview/nf-certview-ienumcertviewattribute-skip">IEnumCERTVIEWATTRIBUTE::Skip</a>
 

 

