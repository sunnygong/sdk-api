---
UID: NF:lzexpand.GetExpandedNameA
title: GetExpandedNameA function (lzexpand.h)
description: Retrieves the original name of a compressed file, if the file was compressed by the Lempel-Ziv algorithm.
old-location: fs\getexpandedname.htm
tech.root: FileIO
ms.assetid: 173344bc-59ba-46ba-901a-f8a8929bc4ee
ms.date: 12/05/2018
ms.keywords: GetExpandedName, GetExpandedName function [Files], GetExpandedNameA, GetExpandedNameW, _win32_getexpandedname, base.getexpandedname, fs.getexpandedname, lzexpand/GetExpandedName, lzexpand/GetExpandedNameA, lzexpand/GetExpandedNameW
ms.topic: function
f1_keywords:
- lzexpand/GetExpandedName
dev_langs:
- c++
req.header: lzexpand.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetExpandedNameW (Unicode) and GetExpandedNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Lz32.lib
req.dll: Lz32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Lz32.dll
api_name:
- GetExpandedName
- GetExpandedNameA
- GetExpandedNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetExpandedNameA function


## -description


Retrieves the original name of a compressed file, if the file was compressed by the Lempel-Ziv algorithm.


## -parameters




### -param lpszSource [in]

The name of the compressed file.


### -param lpszBuffer [out]

A pointer to a buffer that receives the original name of the compressed file.


## -returns



If the function succeeds, the return value is 1.

If the function fails, the return value is LZERROR_BADVALUE. There is no extended error information for this function; do not call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  <b>GetExpandedName</b> calls neither 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> nor 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setlasterrorex">SetLastErrorEx</a>; thus, its failure does not affect a thread's last-error code.</div>
<div> </div>



## -remarks



The contents of the buffer pointed to by the <i>lpszBuffer</i> parameter is the original file name if the file was compressed by using the <b>/r</b> option. If the <b>/r</b> option was not used, this function duplicates the name in the <i>lpszSource</i> parameter into the <i>lpszBuffer</i> buffer.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
 

 

