---
title: Compilerwarnung (Stufe 2) C4356 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4356
dev_langs: C++
helpviewer_keywords: C4356
ms.assetid: 3af3defe-de33-43b6-bd6c-2c2e09e34f3f
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: cd32ad76e83a51ad361b7d0226fa73fd88b58214
ms.sourcegitcommit: ca2f94dfd015e0098a6eaf5c793ec532f1c97de1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2017
---
# <a name="compiler-warning-level-2-c4356"></a>Compilerwarnung (Stufe 2) C4356
'Member': statische Datenmember kann nicht über eine abgeleitete Klasse initialisiert werden  
  
 Die Initialisierung eines statischen Datenmembers wurde nicht ordnungsgemäß formatiert. Der Compiler akzeptiert die Initialisierung. Um die Warnung zu vermeiden, initialisieren Sie das Element über die Basisklasse aus.  
  
 Verwenden der [Warnung](../../preprocessor/warning.md) Pragma verwenden, um diese Warnung zu unterdrücken.  
  
 Im folgenden Beispiel wird C4356 generiert:  
  
```  
// C4356.cpp  
// compile with: /W2 /EHsc  
#include <iostream>  
  
template <class T>  
class C {  
   static int n;  
};  
  
class D : C<int> {};  
  
int D::n = 0; // C4356  
// try the following line instead  
// int C<int>::n = 0;  
  
class A {  
public:  
   static int n;  
};  
  
class B : public A {};  
  
int B::n = 10;   // C4356  
// try the following line instead  
// int A::n = 99;  
  
int main() {  
   using namespace std;  
   cout << B::n << endl;  
}  
```