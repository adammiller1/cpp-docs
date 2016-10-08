---
title: "Design Principles for Collection and Enumerator Interfaces"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea19a39e-6333-41a1-be62-5435c236640e
caps.latest.revision: 8
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# Design Principles for Collection and Enumerator Interfaces
There are different design principles behind each type of interface:  
  
-   A collection interface provides *random* access to a *single* item in the collection via the **Item** method, it lets clients discover how many items are in the collection via the **Count** property, and often allows clients to add and remove items.  
  
-   An enumerator interface provides *serial* access to *multiple* items in a collection, it doesn't allow the client to discover how many items are in the collection (until the enumerator stops returning items), and it doesn't provide any way of adding or removing items.  
  
 Each type of interface plays a different role in providing access to the elements in a collection.  
  
## See Also  
 [Collections and Enumerators](../VS_visualcpp/ATL-Collections-and-Enumerators.md)