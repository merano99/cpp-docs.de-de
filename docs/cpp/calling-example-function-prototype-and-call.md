---
title: 'Aufrufbeispiel: Funktionsprototyp und Aufruf-Funktion | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- calling conventions, examples [C++]
- examples [C++], calling conventions
ms.assetid: e4275d1f-df2e-4bfc-a162-eb43ec69554a
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: 897771dbe2d769744bd5dc119083c9db243d56c0
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="calling-example-function-prototype-and-call"></a>Aufrufbeispiel:Funktionsprototyp und Aufruf
## <a name="microsoft-specific"></a>Microsoft-spezifisch  
 Das folgende Beispiel zeigt die Ergebnisse eines Funktionsaufrufs mit unterschiedlichen Aufrufkonventionen.  
  
 Dieses Beispiel basiert auf dem folgenden Funktionsskelett. Ersetzen Sie `calltype` durch die entsprechende Aufrufkonvention.  
  
```  
void    calltype MyFunc( char c, short s, int i, double f );  
.  
.  
.  
void    MyFunc( char c, short s, int i, double f )  
    {  
    .  
    .  
    .  
    }  
.  
.  
.  
MyFunc ('x', 12, 8192, 2.7183);  
```  
  
 Weitere Informationen finden Sie unter [Ergebnisse aufrufen Beispiel](../cpp/results-of-calling-example.md).  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Aufrufkonventionen](../cpp/calling-conventions.md)