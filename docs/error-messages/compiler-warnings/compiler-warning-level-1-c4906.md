---
title: Compilerwarnung (Stufe 1) C4906 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4906
dev_langs: C++
helpviewer_keywords: C4906
ms.assetid: 05318e74-799b-412a-9dce-f02b8161d762
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 784bce01aa18991a28e4410f9fbaf3eb502ddd60
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-level-1-c4906"></a>Compilerwarnung (Stufe 1) C4906

          Zeichenfolgenliteral umgewandelt zu "LPWSTR"  
  
 Der Compiler hat eine unsichere Typumwandlung erkannt. Die Umwandlung erfolgreich war, aber Sie sollten eine Konvertierungsroutine verwenden.  
  
 Diese Warnung ist standardmäßig deaktiviert. Weitere Informationen finden Sie unter [Standardmäßig deaktivierte Compilerwarnungen](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4906 generiert:  
  
```  
// C4906.cpp  
// compile with: /W1  
#pragma warning(default : 4906)  
#include <windows.h>  
#include <stdlib.h>  
#include <stdio.h>  
  
int main()  
{  
    LPWSTR x = (LPWSTR)"1234";   // C4906  
  
    // try the following lines instead  
    // char y[128];  
    // size_t numberOfCharConverted = 0;  
    // errcode err = 0;  
    // err = wcstombs_s(&numberOfCharConverted , &y[0], 128,  
    //                  L"12345", 4);  
    // if (err != 0)  
    // {  
    //     printf_s("wcstombs_s failed!");  
    //     return -1;  
    // }  
    // printf_s("%s\n", y);  
  
    return 0;  
}  
```