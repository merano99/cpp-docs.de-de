---
title: Compilerwarnung (Stufe 1) C4558 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4558
dev_langs: C++
helpviewer_keywords: C4558
ms.assetid: 52bb0324-7bec-468c-b35b-13a08d38e578
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 77936e230af6a34b5bc48a5d79ee077882845294
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-level-1-c4558"></a>Compilerwarnung (Stufe 1) C4558
Wert des Operanden 'Value' ist außerhalb des gültigen Bereichs "Untergrenze - Obergrenze"  
  
 Die an eine Anweisung Assemblysprache übergebene Wert ist außerhalb des Bereichs für den Parameter angegeben. Der Wert wird abgeschnitten.  
  
 Im folgenden Beispiel wird C4558 generiert:  
  
```  
// C4558.cpp  
// compile with: /W1  
// processor: x86  
void asm_test() {  
   __asm pinsrw   mm1, eax, 8;   // C4558  
}  
  
int main() {  
}  
```