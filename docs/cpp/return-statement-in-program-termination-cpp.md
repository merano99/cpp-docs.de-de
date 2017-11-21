---
title: return-Anweisung in Programmbeendigung (C++) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
helpviewer_keywords:
- data types [C++], function return types
- function return types [C++], return statement
- return keyword [C++], syntax
ms.assetid: 66d002ab-5625-4b68-8446-71e1b8fcdbd8
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: cb3555ecb80b2f6bc8663325b500ffb2eb317ce3
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="return-statement-in-program-termination-c"></a>return-Anweisung in Programmbeendigung (C++)
Ausgeben einer `return` -Anweisung vom **main** ist funktionell gleichwertig mit einem Aufruf der **beenden** Funktion. Betrachten Sie das folgende Beispiel:  
  
```  
// return_statement.cpp  
#include <stdlib.h>  
int main()  
{  
    exit( 3 );  
    return 3;  
}  
```  
  
 Die **beenden** und `return` Anweisungen im vorherigen Beispiel funktional identisch sind. Allerdings erfordert C++, dass Funktionen, die andere Rückgabetypen als `void` haben, einen Wert zurückgeben. Die `return` -Anweisung können Sie einen Wert von zurückgeben **main**.  
  
## <a name="see-also"></a>Siehe auch  
 [Programmbeendigung](../cpp/program-termination.md)