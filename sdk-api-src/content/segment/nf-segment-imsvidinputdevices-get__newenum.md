---
UID: NF:segment.IMSVidInputDevices.get__NewEnum
title: IMSVidInputDevices::get__NewEnum (segment.h)
description: The get__NewEnum method retrieves an enumerator for the collection.
old-location: mstv\imsvidinputdevices_get__newenum.htm
tech.root: mstv
ms.assetid: a33c9549-c5a6-48c1-bf49-66a7bf81cdaa
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevices interface [Microsoft TV Technologies],get__NewEnum method, IMSVidInputDevices.get__NewEnum, IMSVidInputDevices::get__NewEnum, IMSVidInputDevicesget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],IMSVidInputDevices interface, mstv.imsvidinputdevices_get__newenum, segment/IMSVidInputDevices::get__NewEnum
ms.topic: method
f1_keywords:
- segment/IMSVidInputDevices.get__NewEnum
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- COM
api_location:
- segment.h
api_name:
- IMSVidInputDevices.get__NewEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidInputDevices::get__NewEnum


## -description


The <b>get__NewEnum</b> method retrieves an enumerator for the collection.


## -parameters




### -param pD [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method is provided so that Automation clients can iterate through the collection using a <code>For...Each</code> loop.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread. (C++ applications should generally use the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidinputdevices-get_item">IMSVidInputDevices::get_Item</a> method instead.)

If the method succeeds, the <b>IEnumVARIANT</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices Interface</a>
 

 

