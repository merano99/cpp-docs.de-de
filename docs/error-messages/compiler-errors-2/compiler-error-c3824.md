---
title: Compilerfehler C3824 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3824
dev_langs:
- C++
helpviewer_keywords:
- C3824
ms.assetid: b6c6adf1-0a29-401c-a06e-616fd50d4c37
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 529e881d8872d3ea1d69da14ac393282c4f3efc1
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3824"></a>Compilerfehler C3824
'Member': Dieser Typ darf nicht in diesem Kontext (Funktionsparameter, Rückgabetyp oder einen statischen Member)  
  
 Feste Zeiger nicht Parameter und Rückgabetypen oder deklariert `static`.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3824 generiert:  
  
```  
// C3824a.cpp  
// compile with: /clr /c  
void func() {  
   static pin_ptr<int> a; // C3824  
   pin_ptr<int> b; // OK  
}  
```  
