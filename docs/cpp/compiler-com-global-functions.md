---
title: "Compiler COM Global Functions"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "cl.exe compiler, COM support"
  - "COM, compiler support"
ms.assetid: 74449d26-50a2-47c7-b175-7cf2cf83533e
caps.latest.revision: 7
ms.author: "mblome"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Compiler COM Global Functions
**Microsoft Specific**  
  
 The following routines are available:  
  
|Function|Description|  
|--------------|-----------------|  
|[_com_raise_error](../cpp/_com_raise_error.md)|Throws a [_com_error](../cpp/_com_error-class.md) in response to a failure.|  
|[_set_com_error_handler](../cpp/_set_com_error_handler.md)|Replaces the default function that is used for COM error-handling.|  
|[ConvertBSTRToString](../cpp/convertbstrtostring.md)|Converts a `BSTR` value to a **char \***.|  
|[ConvertStringToBSTR](../cpp/convertstringtobstr.md)|Converts a **char \*** value to a `BSTR`.|  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler COM Support Classes](../cpp/compiler-com-support-classes.md)   
 [Compiler COM Support](../cpp/compiler-com-support.md)