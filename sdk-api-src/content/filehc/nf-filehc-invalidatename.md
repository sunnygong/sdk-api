---
UID: NF:filehc.InvalidateName
title: InvalidateName function (filehc.h)
description: Enables the user to remove a single name and all associated data from the name cache.
old-location: winprog\_invalidatename.htm
tech.root: DevNotes
ms.assetid: 86c6eccf-5c4a-421b-b8e2-762ea5b77bf3
ms.date: 12/05/2018
ms.keywords: InvalidateName, InvalidateName function [Windows API], filehc/InvalidateName, winprog._invalidatename
ms.topic: function
f1_keywords:
- filehc/InvalidateName
dev_langs:
- c++
req.header: filehc.h
req.include-header: 
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
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Fcachdll.dll
api_name:
- InvalidateName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InvalidateName function


## -description


Enables the user to remove a single name and all associated data from the name cache.


## -parameters




### -param pNameCache [in]

A pointer to the name cache that the client will use.


### -param lpbName [in]

The bytes that the user provides for the name of the cache item.


### -param cbName [in]

The actual byte count of the name.


## -returns



Returns <b>TRUE</b> if the name and associated data are removed from the name cache; otherwise, it returns <b>FALSE</b>.



