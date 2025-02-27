---
UID: NF:synchapi.InitOnceExecuteOnce
title: InitOnceExecuteOnce function (synchapi.h)
description: Executes the specified function successfully one time. No other threads that specify the same one-time initialization structure can execute the specified function while it is being executed by the current thread.
old-location: base\initonceexecuteonce.htm
tech.root: Sync
ms.assetid: 04c161ed-d1b0-4995-b246-cb64cb67ae47
ms.date: 12/05/2018
ms.keywords: InitOnceExecuteOnce, InitOnceExecuteOnce function, base.initonceexecuteonce, synchapi/InitOnceExecuteOnce, winbase/InitOnceExecuteOnce
ms.topic: function
f1_keywords:
- synchapi/InitOnceExecuteOnce
dev_langs:
- c++
req.header: synchapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Synch-l1-2-0.dll
- KernelBase.dll
- API-MS-Win-Core-Synch-l1-2-1.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- InitOnceExecuteOnce
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InitOnceExecuteOnce function


## -description


Executes the specified function successfully one time. No other threads that specify the same one-time initialization structure can execute the specified function while it is being executed by the current thread.


## -parameters




### -param InitOnce [in, out]

A pointer to the one-time initialization structure.


### -param InitFn [in]

A pointer to an application-defined <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nc-synchapi-pinit_once_fn">InitOnceCallback</a> function.


### -param Context [out, optional]

A parameter that receives data stored with the one-time initialization structure upon success. The low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> bits of the data are always zero.


### -param Parameter [in, out, optional]

A parameter to be passed to the callback function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function is used for synchronous one-time initialization. For asynchronous one-time initialization, use the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initoncebegininitialize">InitOnceBeginInitialize</a> function with the <b>INIT_ONCE_ASYNC</b> flag.

Only one thread at a time can execute the callback function specified by <i>InitFn</i>. Other threads that specify the same one-time initialization structure block until the callback finishes.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/using-one-time-initialization">Using One-Time Initialization</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nc-synchapi-pinit_once_fn">InitOnceCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initonceinitialize">InitOnceInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/one-time-initialization">One-Time Initialization</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

