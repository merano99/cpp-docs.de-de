---
title: Compilerfehler C2434 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2434
dev_langs:
- C++
helpviewer_keywords:
- C2434
ms.assetid: 01329e26-7c74-4219-b74f-69e3a40c9738
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 954ef1f8db47c5cd9c420e8099cc3060ebb8a32b
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2434"></a>Compilerfehler C2434
'Symbol': ein Symbol mit __declspec(process) deklariertes kann nicht initialisiert werden, dynamisch in/CLR: pure-Modus  
  
 Die Compileroptionen **/clr:pure** und **/clr:safe** sind in Visual Studio 2015 veraltet.  
  
 Es ist nicht möglich, eine Variable pro-Prozess unter dynamisch zu initialisieren **/CLR: pure**. Weitere Informationen finden Sie unter [/CLR (Common Language Runtime-Kompilierung)](../../build/reference/clr-common-language-runtime-compilation.md) und [Prozess](../../cpp/process.md).  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2434 generiert.  
  
```  
// C2434.cpp  
// compile with: /clr:pure /c  
int f() { return 0; }  
__declspec(process) int i = f();   // C2434  
__declspec(process) int i2 = 0;   // OK  
```