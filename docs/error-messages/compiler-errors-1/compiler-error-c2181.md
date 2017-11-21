---
title: Compilerfehler C2181 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2181
dev_langs:
- C++
helpviewer_keywords:
- C2181
ms.assetid: d52b2fe4-566a-40a9-b8e2-8dce1f287668
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 2a488fbca338c5f44c89b60181f034a48203bb3c
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2181"></a>Compilerfehler C2181
Ungültiges "else" ohne zugehöriges "if"  
  
 Zu jedem `else` -Element muss ein zugehöriges `if`-Element vorhanden sein.  
  
 Im folgenden Beispiel wird C2181 generiert:  
  
```  
// C2181.cpp  
int main() {  
   int i = 0;  
   else   // C2181  
      i = 1;  
}  
```  
  
 Mögliche Lösung:  
  
```  
// C2181b.cpp  
int main() {  
   int i = 0;  
   if(i)  
      i = 0;  
   else  
      i = 1;  
}  
```