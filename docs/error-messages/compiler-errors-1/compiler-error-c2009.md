---
title: Compiler-Fehler C2009 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2009
dev_langs:
- C++
helpviewer_keywords:
- C2009
ms.assetid: fe9d94ed-20a5-4d83-b9c4-60ee69d2f30a
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 2bbae441d7b4c9e57a4080dd643f6563eed6c48e
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2009"></a>Compiler-Fehler C2009 generiert
Mehrfachverwendung des formalen Makroparameters "identifier"  
  
 Den Bezeichner wird von die Liste der formalen Parameter einer Makrodefinition mehrmals verwendet. Bezeichner in der Parameterliste für das Makro müssen eindeutig sein.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2009 generiert:  
  
```  
// C2009.cpp  
#include <stdio.h>  
  
#define macro1(a,a) (a*a)   // C2009  
  
int main()   
{  
    printf_s("%d\n", macro1(2));  
}  
```  
  
## <a name="example"></a>Beispiel  
 Mögliche Lösung:  
  
```  
// C2009b.cpp  
#include <stdio.h>  
  
#define macro2(a)   (a*a)   
#define macro3(a,b) (a*b)  
  
int main()   
{  
    printf_s("%d\n", macro2(2));  
    printf_s("%d\n", macro3(2,4));  
}  
```