---
title: "improper_scheduler_attach Class"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "concrt/concurrency::improper_scheduler_attach"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "improper_scheduler_attach class"
ms.assetid: 5a76da0a-091b-4748-8f62-b3a28f674f9e
caps.latest.revision: 18
ms.author: "mithom"
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
# improper_scheduler_attach Class
This class describes an exception thrown when the `Attach` method is called on a `Scheduler` object which is already attached to the current context.  
  
## Syntax  
  
```
class improper_scheduler_attach : public std::exception;
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[improper_scheduler_attach::improper_scheduler_attach Constructor](#improper_scheduler_attach__improper_scheduler_attach_constructor)|Overloaded. Constructs an `improper_scheduler_attach` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `improper_scheduler_attach`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="improper_scheduler_attach__improper_scheduler_attach_constructor"></a>  improper_scheduler_attach::improper_scheduler_attach Constructor  
 Constructs an `improper_scheduler_attach` object.  
  
```
explicit _CRTIMP improper_scheduler_attach(_In_z_ const char* _Message) throw();

improper_scheduler_attach() throw();
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../parallel/concurrency-namespace.md)   
 [Scheduler Class](../parallel/scheduler-class.md)   
 [Scheduler::Attach Method](../parallel/scheduler-class.md#scheduler__attach_method)
