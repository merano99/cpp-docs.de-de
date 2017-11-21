---
title: Compilerfehler C2264 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2264
dev_langs: C++
helpviewer_keywords: C2264
ms.assetid: 158b72cc-cee9-4a08-bd79-b7a5955345a8
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: d30af255e8dcf8b46748b0d59126f53d4c15eab2
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2264"></a>Compilerfehler C2264
'Funktion': Fehler in der Funktionsdefinition oder-Deklaration; Funktion wird nicht aufgerufen.  
  
 Die Funktion kann aufgrund einer falschen Definition oder Deklaration aufgerufen werden.  
  
 Im folgende Beispiel wird C2264 generiert:  
  
```  
// C2264.cpp  
struct C {  
   // Delete the following line to resolve.  
   operator int(int = 0){}   // incorrect declaration  
};  
  
struct D {  
   operator int(){return 0;}   // OK  
};  
  
int main() {  
   int i;  
  
   C c;  
   i = c;   // C2264  
  
   D d;  
   i = d;   // OK  
}  
```