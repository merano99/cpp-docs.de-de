---
title: Compilerfehler C2148 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2148
dev_langs: C++
helpviewer_keywords: C2148
ms.assetid: e510c2c9-7b57-4ce8-be03-ba363e2cc5d9
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 2d98197ed8043af05fd27239ca10aa3a0d06e3c0
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2148"></a>Compilerfehler C2148
Gesamtgröße des Arrays darf 0x7fffffff Bytes nicht überschreiten.  
  
 Ein Array überschreitet den Grenzwert. Reduzieren Sie die Größe des Arrays.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2148 generiert:  
  
```  
// C2148.cpp  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( ) {  
   char MyArray[0x7ffffffff];   // C2148  
   char * MyArray2 = (char *)malloc(0x7fffffff);  
  
   if (MyArray2)  
      printf_s("It worked!");  
   else  
      printf_s("It didn't work.");  
}  
```