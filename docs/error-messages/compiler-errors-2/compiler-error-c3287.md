---
title: Compilerfehler C3287 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3287
dev_langs:
- C++
helpviewer_keywords:
- C3287
ms.assetid: c1fa73d2-2c82-4136-a7da-0e75e3b420ad
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: b09d2af16ca6d38e476e7298b2b5fb61b2b30129
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3287"></a>Compilerfehler C3287
Der Typ 'Typ' (Rückgabetyp von 'GetEnumerator') muss eine passende öffentliche MoveNext-Memberfunktion und eine öffentliche Current-Eigenschaft aufweisen.  
  
 Benutzerdefinierte Auflistungsklassen müssen Definitionen für `MoveNext` und `Current`enthalten.  
  
 Weitere Informationen finden Sie unter [How to: Iterate Over a User-Defined Collection with for each](../../dotnet/how-to-iterate-over-a-user-defined-collection-with-for-each.md) .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3287 generiert:  
  
```  
// C3287.cpp  
// compile with: /clr  
using namespace System;  
  
ref struct R {  
   bool MoveNext() {  
      return true;  
   }  
   property Object^ Current {  
      Object^ get() {  
         Object ^ o = gcnew Object;  
         return o;  
      }  
   }  
};  
  
ref struct R2 {  
   R ^GetEnumerator() {  
      R^ r = gcnew R;  
      return r;  
   }  
};  
  
ref struct T {};  
  
ref struct T2 {  
   T ^GetEnumerator() {  
      T^ t = gcnew T;  
      return t;  
   }  
};  
  
int main() {  
   for each (int i in gcnew T2) {}   // C3287  
   for each (int i in gcnew R2) {}   // OK  
}  
```