---
title: Compilerfehler C3740 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3740
dev_langs:
- C++
helpviewer_keywords:
- C3740
ms.assetid: edb17a90-2307-4df6-943d-580460d26d2b
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 1466945e3b6647bedccd65e899bb3eb78ac28de1
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3740"></a>Compilerfehler C3740
Vorlagen können keine Datenquelle oder Ereignisse empfangen  
  
 Eine aus einer Vorlage gebildete Klasse oder Struktur kann keine enthalten [Ereignisse](../../cpp/event-handling.md).  
  
 Im folgende Beispiel wird C3740 generiert:  
  
```  
// C3740.cpp  
template <typename T>   // Delete the template specification  
struct E {  
   __event void f();   // C3740  
};  
  
int main() {  
}  
```