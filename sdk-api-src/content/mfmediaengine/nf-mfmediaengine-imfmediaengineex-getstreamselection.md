---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStreamSelection
title: IMFMediaEngineEx::GetStreamSelection (mfmediaengine.h)
description: Queries whether a stream is selected to play.
old-location: mf\imfmediaengineex_getstreamselection.htm
tech.root: medfound
ms.assetid: 93EA1E19-4333-484D-96C8-3244F7C040EF
ms.date: 12/05/2018
ms.keywords: FALSE, GetStreamSelection, GetStreamSelection method [Media Foundation], GetStreamSelection method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStreamSelection method, IMFMediaEngineEx.GetStreamSelection, IMFMediaEngineEx::GetStreamSelection, TRUE, mf.imfmediaengineex_getstreamselection, mfmediaengine/IMFMediaEngineEx::GetStreamSelection
ms.topic: method
f1_keywords:
- mfmediaengine/IMFMediaEngineEx.GetStreamSelection
dev_langs:
- c++
req.header: mfmediaengine.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFMediaEngineEx.GetStreamSelection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::GetStreamSelection


## -description


Queries whether a stream is selected to play.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. To get the number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getnumberofstreams">IMFMediaEngineEx::GetNumberOfStreams</a>.


### -param pEnabled [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The stream is selected. During playback, this stream will play.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The stream is not selected. During playback, this stream will not play.


</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

