---
title: "Compilerwarnung (Stufe 1) C4537 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4537"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4537"
ms.assetid: 9454493c-d419-475e-8f35-9c00233c9329
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerwarnung (Stufe 1) C4537
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Objekt': 'Operator' angewendet auf Nicht\-UDT\-Typ  
  
 Ein Verweis wurde übergeben, obwohl ein Objekt \(benutzerdefinierter Typ\) erwartet wurde.  Ein Verweis ist kein Objekt, diese Unterscheidung kann vom Inlineassemblercode jedoch nicht getroffen werden.  Der Compiler generiert Code so, als wäre das ***Objekt*** eine Instanz.  
  
 Im folgenden Beispiel wird C4537 generiert:  
  
```  
// C4537.cpp  
// compile with: /W1 /c  
// processor: x86  
struct S {  
   int member;  
};  
  
void f1(S &s) {  
   __asm mov eax, s.member;   // C4537  
   // try the following code instead  
   // or, make the declaration "void f1(S s)"  
   /*  
   mov eax, s  
   mov eax, [eax]s.member  
   */  
}  
```