---
title: "tmpfile_s"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - tmpfile_s
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr100_clr0400.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr120_clr0400.dll
  - ucrtbase.dll
  - api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
ms.assetid: 50879c69-215e-425a-a2a3-8b5467121eae
caps.latest.revision: 18
manager: ghogen
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# tmpfile_s
Creates a temporary file. It is a version of [tmpfile](../VS_visualcpp/tmpfile.md) with security enhancements as described in [Security Features in the CRT](../VS_visualcpp/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t tmpfile_s(  
   FILE** pFilePtr  
);  
```  
  
#### Parameters  
 [out] `pFilePtr`  
 The address of a pointer to store the address of the generated pointer to a stream.  
  
## Return Value  
 Returns 0 if successful, an error code on failure.  
  
### Error Conditions  
  
|`pFilePtr`|**Return Value**|**Contents of**  `pFilePtr`|  
|----------------|----------------------|---------------------------------|  
|`NULL`|`EINVAL`|not changed|  
  
 If the above parameter validation error occurs, the invalid parameter handler is invoked, as described in [Parameter Validation](../VS_visualcpp/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the return value is `EINVAL`.  
  
## Remarks  
 The `tmpfile_s` function creates a temporary file and puts a pointer to that stream in the `pFilePtr` argument. The temporary file is created in the root directory. To create a temporary file in a directory other than the root, use [tmpnam_s](../VS_visualcpp/tmpnam_s--_wtmpnam_s.md) or [tempnam](../VS_visualcpp/_tempnam--_wtempnam--tmpnam--_wtmpnam.md) in conjunction with [fopen](../VS_visualcpp/fopen--_wfopen.md).  
  
 If the file cannot be opened, `tmpfile_s` writes `NULL` to the `pFilePtr` parameter. This temporary file is automatically deleted when the file is closed, when the program terminates normally, or when `_rmtmp` is called, assuming that the current working directory does not change. The temporary file is opened in `w+b` (binary read/write) mode.  
  
 Failure can occur if you attempt more than `TMP_MAX_S` (see STDIO.H) calls with `tmpfile_s.`  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`tmpfile_s`|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../VS_visualcpp/Compatibility.md) in the Introduction.  
  
## Example  
  
> [!NOTE]
>  This example requires administrative privileges to run on Windows Vista.  
  
```  
// crt_tmpfile_s.c  
// This program uses tmpfile_s to create a  
// temporary file, then deletes this file with _rmtmp.  
//  
  
#include <stdio.h>  
  
int main( void )  
{  
   FILE *stream;  
   char tempstring[] = "String to be written";  
   int  i;  
   errno_t err;  
  
   // Create temporary files.  
   for( i = 1; i <= 3; i++ )  
   {  
      err = tmpfile_s(&stream);  
      if( err )  
         perror( "Could not open new temporary file\n" );  
      else  
         printf( "Temporary file %d was created\n", i );  
   }  
  
   // Remove temporary files.  
   printf( "%d temporary files deleted\n", _rmtmp() );  
}  
```  
  
 **Temporary file 1 was created**  
**Temporary file 2 was created**  
**Temporary file 3 was created**  
**3 temporary files deleted**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md).  
  
## See Also  
 [Stream I/O](../VS_visualcpp/Stream-I-O.md)   
 [_rmtmp](../VS_visualcpp/_rmtmp.md)   
 [_tempnam, _wtempnam, tmpnam, _wtmpnam](../VS_visualcpp/_tempnam--_wtempnam--tmpnam--_wtmpnam.md)