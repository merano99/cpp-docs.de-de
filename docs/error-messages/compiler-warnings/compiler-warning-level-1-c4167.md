---
title: Compilerwarnung (Stufe 1) C4167 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4167
dev_langs:
- C++
helpviewer_keywords:
- C4167
ms.assetid: 74a420bd-9371-4167-b1ee-74dd8680f97b
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 154b0b55bcdfe1b69fc84ca8e11808fa0343265c
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4167"></a>Compilerwarnung (Stufe 1) C4167
Funktion: Nur als systeminterne Funktion verfügbar  
  
 Die **#pragma-Funktion** versucht zu erzwingen, dass der Compiler einen konventionellen Aufruf für eine Funktion verwendet, die in systeminterner Form verwendet werden muss. Das Pragma wird ignoriert.  
  
 Um diese Warnung zu vermeiden, entfernen Sie die **#pragma-Funhtion**.  
  
## <a name="example"></a>Beispiel  
  
```  
// C4167.cpp  
// compile with: /W1  
#include <malloc.h>  
#pragma function(_alloca )   // C4167: _alloca() is intrinsic only  
int main(){}  
```