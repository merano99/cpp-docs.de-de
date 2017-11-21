---
title: Compilerfehler C3536 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3536
dev_langs: C++
helpviewer_keywords: C3536
ms.assetid: 8d866075-866b-49eb-9979-ee27b308f7e3
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 90db065c9a16e72a396bd1c1ae54bb99cdb97153
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3536"></a>Compilerfehler C3536
'Symbol': kann nicht vor der Initialisierung verwendet werden  
  
 Das angegebene Symbol kann nicht verwendet werden, vor der Initialisierung. In der Praxis bedeutet dies, dass eine Variable nicht verwendet werden kann, um sich selbst zu initialisieren.  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
1.  Initialisieren Sie eine Variable mit sich selbst nicht.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3536 erzeugt, da jede Variable mit sich selbst initialisiert wird.  
  
```  
// C3536.cpp  
// Compile with /Zc:auto  
int main()  
{  
   auto a = a;     //C3536  
   auto b = &b;    //C3536  
   auto c = c + 1; //C3536  
   auto* d = &d;   //C3536  
   auto& e = e;    //C3536  
   return 0;  
};  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Auto-Schlüsselwort](../../cpp/auto-keyword.md)