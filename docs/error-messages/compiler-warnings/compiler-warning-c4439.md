---
title: Compilerwarnung C4439 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4439
dev_langs: C++
helpviewer_keywords: C4439
ms.assetid: 9449958f-f407-4824-829b-9e092f2af97d
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: eec228922a6f5796587243fe2d1f2c6cc1cf6b1c
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-c4439"></a>Compilerwarnung C4439
'Funktion': Definition der Funktion mit einem verwalteten Typ in der Signatur benötigen eine __clrcall-Aufrufkonvention  
  
 Der Compiler implizit eine Aufrufkonvention mit ersetzt [__clrcall](../../cpp/clrcall.md). Um diese Warnung zu beheben, entfernen die `__cdecl` oder `__stdcall` Aufrufkonvention.  
  
 C4439 wird immer als Fehler ausgegeben. Sie können diese Warnung mit Deaktivieren der `#pragma warning` oder **/WD**; finden Sie unter [Warnung](../../preprocessor/warning.md) oder  [ /w, / W0, /W1, /W2, /W3, / W4, /w1, /w2, /w3, / W4, / Wall, / WD, / we, /, wo WV, / WX (Warnstufe)](../../build/reference/compiler-option-warning-level.md)für Weitere Informationen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4439 generiert.  
  
```  
// C4439.cpp  
// compile with: /clr  
void __stdcall f( System::String^ arg ) {}   // C4439  
void __clrcall f2( System::String^ arg ) {}   // OK  
void f3( System::String^ arg ) {}   // OK  
```