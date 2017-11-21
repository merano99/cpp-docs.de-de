---
title: Compilerfehler C2250 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2250
dev_langs:
- C++
helpviewer_keywords:
- C2250
ms.assetid: f990986f-5c7d-4af4-a25c-b35540f1e217
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 8a0d72b1bc986ec9ca3a2be5ffa0454cabad0def
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2250"></a>Compilerfehler C2250
'Bezeichner': Mehrdeutige Vererbung von 'class:: Member'  
  
 Die abgeleitete Klasse erbt mehr als eine Überschreibung einer virtuellen Funktion einer virtuellen Basisklasse. Diese Außerkraftsetzungen sind mehrdeutig, in der abgeleiteten Klasse.  
  
 Im folgenden Beispiel wird C2286 generiert:  
  
```  
// C2250.cpp  
// compile with: /c  
// C2250 expected  
struct V {  
   virtual void vf();  
};  
  
struct A : virtual V {  
   void vf();  
};  
  
struct B : virtual V {  
   void vf();  
};  
  
struct D : A, B {  
   // Uncomment the following line to resolve.  
   // void vf();  
};  
```