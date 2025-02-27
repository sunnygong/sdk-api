---
UID: NF:wuapi.IAutomaticUpdates.Resume
title: IAutomaticUpdates::Resume (wuapi.h)
description: Restarts automatic updating if automatic updating is paused.
old-location: wua\iautomaticupdates_resume.htm
tech.root: Wua_Sdk
ms.assetid: 8aabfb89-89e2-450e-bfe6-62a48f93746f
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdates interface [Windows Update Agent],Resume method, IAutomaticUpdates.Resume, IAutomaticUpdates::Resume, Resume, Resume method [Windows Update Agent], Resume method [Windows Update Agent],IAutomaticUpdates interface, wua.iautomaticupdates_resume, wuapi/IAutomaticUpdates::Resume
ms.topic: method
f1_keywords:
- wuapi/IAutomaticUpdates.Resume
dev_langs:
- c++
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IAutomaticUpdates.Resume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutomaticUpdates::Resume


## -description


<p class="CCE_Message">[<b>IAutomaticUpdates::Resume</b> is no longer supported. Starting with 
    Windows 10 calls to <b>Resume</b> always return 
    <b>S_OK</b>, but do nothing.]

Restarts automatic updating if automatic updating is paused.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_AU_PAUSED</b></dt>
</dl>
</td>
<td width="60%">
Automatic Updates is paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_LEGACYSERVER</b></dt>
</dl>
</td>
<td width="60%">
You cannot search for updates if the following conditions are true:

<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serverselection">ServerSelection</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is set to <a href="https://docs.microsoft.com/windows/desktop/api/wuapicommon/ne-wuapicommon-serverselection">ssManagedServer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapicommon/ne-wuapicommon-serverselection">ssDefault</a>.</li>
<li>The managed server on a computer is a Microsoft Software Update Services (SUS) 1.0 server.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



This method requires administrator permissions.

Callers should call <b>Resume</b> after calling the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-pause">Pause</a> method as soon as they no longer need to pause automatic updating.

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface has been locked down.

 This method returns <b>WU_E_AU_NOSERVICE</b> if Automatic Updates is disabled, initializing, uninitializing, or not configured.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">IAutomaticUpdates</a>
 

 

