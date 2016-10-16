---
title: "MutexTraits Structure"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "MutexTraits structure"
ms.assetid: 6582df80-b9ba-4892-948f-d572a3b23d54
caps.latest.revision: 3
ms.author: "mblome"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# MutexTraits Structure
Defines common characteristics of the [Mutex](../windows/mutex-class1.md) class.  
  
## Syntax  
  
```  
struct MutexTraits : HANDLENullTraits;  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[MutexTraits::Unlock Method](../windows/mutextraits--unlock-method.md)|Releases exclusive control of a shared resource.|  
  
## Inheritance Hierarchy  
 `HANDLENullTraits`  
  
 `MutexTraits`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## See Also  
 [Microsoft::WRL::Wrappers::HandleTraits Namespace](../windows/microsoft--wrl--wrappers--handletraits-namespace.md)