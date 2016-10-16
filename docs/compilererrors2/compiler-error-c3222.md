---
title: "Compiler Error C3222"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "error-reference"
f1_keywords: 
  - "C3222"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3222"
ms.assetid: 5624bde8-2fd0-4b8b-92ce-5dfbaf91cf93
caps.latest.revision: 10
ms.author: "corob"
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
# Compiler Error C3222
'parameter' : cannot declare default arguments for member functions of a managed or WinRT type or generic functions  
  
 It is not permitted to declare a method parameter with a default argument. An overloaded form of the method is one way to work around this issue. That is, define a method with the same name with no parameters and then initialize the variable in the method body.  
  
 The following sample generates C3222:  
  
```  
// C3222_2.cpp  
// compile with: /clr  
public ref class G {  
   void f( int n = 0 );   // C3222  
};  
```  
  
 The following sample generates C3222:  
  
```  
// C3222.cpp  
// compile with: /clr:oldSyntax  
public __gc class G {  
   void f( int n = 0 );   // C3222  
};  
```