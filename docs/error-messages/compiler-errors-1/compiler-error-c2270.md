---
title: Compilerfehler C2270 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2270
dev_langs:
- C++
helpviewer_keywords:
- C2270
ms.assetid: b52c068e-0b61-42e7-b775-4d57b3ddcba0
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: bc380d8a44e61ac0f709b8440d788d12f3795922
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2270"></a>Compilerfehler C2270
'Funktion': Modifizierer für nicht-Member-Funktionen nicht zulässig  
  
 Eine nicht-Member-Funktion wird deklariert, wobei [const](../../cpp/const-cpp.md), [volatile](../../cpp/volatile-cpp.md), oder eine andere Modifizierers.  
  
 Im folgende Beispiel wird C2270 generiert:  
  
```  
// C2270.cpp  
// compile with: /c  
void func1(void) const;   // C2270, nonmember function  
  
void func2(void);  
  
class CMyClass {  
public:  
   void func2(void) const;  
};  
```