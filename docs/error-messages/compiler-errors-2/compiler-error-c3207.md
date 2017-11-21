---
title: Compilerfehler C3207 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3207
dev_langs:
- C++
helpviewer_keywords:
- C3207
ms.assetid: 4a28b976-142a-4cff-aa2f-480b892c50ca
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 7d0f50d73f32a388669ea49af737b69b57d6a64d
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3207"></a>Compilerfehler C3207
„function“: Ungültiges Vorlagenargument für „arg“, Klassenvorlage wurde erwartet.  
  
 Eine Vorlagenfunktion wurde so definiert, dass sie ein template-Vorlagenargument erwartet. Übergeben wurde aber ein template-Typargument.  
  
 Im folgenden Beispiel wird C3207 generiert:  
  
```  
// C3207.cpp  
template <template <class T> class TT>  
void f(){}  
  
template <class T>  
struct S  
{  
};  
  
void f1()  
{  
   f<S<int> >();   // C3207  
   // try the following line instead  
   // f<S>();  
}  
```