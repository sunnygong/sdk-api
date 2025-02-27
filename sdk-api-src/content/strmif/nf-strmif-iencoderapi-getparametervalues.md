---
UID: NF:strmif.IEncoderAPI.GetParameterValues
title: IEncoderAPI::GetParameterValues (strmif.h)
description: The GetParameterValues method retrieves the list of values supported by the given parameter.
old-location: mstv\iencoderapi_getparametervalues.htm
tech.root: mstv
ms.assetid: 406316b5-1de0-4a89-b1bc-2f3b63ab0739
ms.date: 12/05/2018
ms.keywords: GetParameterValues, GetParameterValues method [Microsoft TV Technologies], GetParameterValues method [Microsoft TV Technologies],IEncoderAPI interface, IEncoderAPI interface [Microsoft TV Technologies],GetParameterValues method, IEncoderAPI.GetParameterValues, IEncoderAPI::GetParameterValues, IEncoderAPIGetParameterValues, mstv.iencoderapi_getparametervalues, strmif/IEncoderAPI::GetParameterValues
ms.topic: method
f1_keywords:
- strmif/IEncoderAPI.GetParameterValues
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IEncoderAPI.GetParameterValues
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEncoderAPI::GetParameterValues


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>.]

The <b>GetParameterValues</b> method retrieves the list of values supported by the given parameter.


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the parameter.
          


### -param Values [out]

Address of a pointer to an array that receives the values.
          


### -param ValuesCount [out]

Indicates the number of entries placed into the array.
            




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns an array of <b>VARIANT</b> types representing the individual values supported by the parameter. This array is allocated by the callee through <b>CoTaskMemAlloc</b> and placed into the <i>Values</i> parameter. On exit, <i>ValuesCount</i> contains the number of elements in the array. The caller must free the array by calling <b>CoTaskMemFree</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI Interface</a>
 

 

