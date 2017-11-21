---
title: Compiler-Fehler C2635 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2635
dev_langs:
- C++
helpviewer_keywords:
- C2635
ms.assetid: 9deca2a8-2d61-42eb-9783-6578132ee3fb
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 8a8ff1361a312c8d2abf7e07de3add2dbd3254ca
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2635"></a>Compiler-Fehler C2635 generiert
Konvertierung einer 'Bezeichner1 *"in einer" Bezeichner2\*"; Konvertierung von einer virtuellen Basisklasse wird impliziert.  
  
 Die Konvertierung erfordert eine Umwandlung aus einem `virtual` Basisklasse in eine abgeleitete Klasse, was nicht zulässig ist.  
  
 Im folgende Beispiel wird C2635 generiert:  
  
```  
// C2635.cpp  
class B {};  
class D : virtual public B {};  
class E : public B {};  
  
int main() {  
   B b;  
   D d;  
   E e;  
  
   D * pD = &d;  
   E * pE = &e;  
   pD = (D*)&b;   // C2635  
   pE = (E*)&b;   // OK  
}  
```