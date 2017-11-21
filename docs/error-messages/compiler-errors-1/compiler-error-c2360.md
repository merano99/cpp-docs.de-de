---
title: Compilerfehler C2360 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2360
dev_langs: C++
helpviewer_keywords: C2360
ms.assetid: 51bfd2ee-8108-4777-aa93-148b9cebfa83
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 12b62d31c125dfc353623fa7cf10fce578698332
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2360"></a>Compilerfehler C2360
Initialisierung von 'Bezeichner' ist 'Case' Bezeichnung übersprungen.  
  
 Die Initialisierung des `identifier` kann übersprungen werden, eine `switch` Anweisung. Sie können nicht hinter einer Deklaration mit einem Initialisierer springen, es sei denn, die Deklaration in einem Block eingeschlossen ist. (Es sei denn, es in einem Block deklariert wird, ist die Variable im Gültigkeitsbereich bis zum Ende der `switch` Anweisung.)  
  
 Im folgende Beispiel wird C2360 generiert:  
  
```  
// C2360.cpp  
int main() {  
   int x = 0;  
   switch ( x ) {  
   case 0 :  
      int i = 1;  
      { int j = 1; }  
   case 1 :   // C2360  
      int k = 1;  
   }  
}  
```  
  
 Mögliche Lösung:  
  
```  
// C2360b.cpp  
int main() {  
   int x = 0;  
   switch ( x ) {  
   case 0 :  
      { int j = 1; int i = 1;}  
   case 1 :  
      int k = 1;  
   }  
}  
```