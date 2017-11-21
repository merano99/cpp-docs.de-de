---
title: Compilerfehler C3734 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3734
dev_langs:
- C++
helpviewer_keywords:
- C3734
ms.assetid: 4e2afdcc-7da9-45a1-9c96-85f25e2986e8
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 83f523bb615ef06716f226d4a6c837acaa26c5b2
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3734"></a>Compilerfehler C3734
„Klasse“: Eine verwaltete oder WinRT-Klasse kann kein „Co-Klasse“-Attribut sein.  
  
 Die [Coclass](../../windows/coclass.md) Attribut kann nicht zusammen mit verwalteten oder WinRT-Klassen.  
  
 Im folgenden Beispiel wird C3734 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C3734.cpp  
// compile with: /clr /c  
[module(name="x")];  
  
[coclass]  
ref class CMyClass {   // C3734 remove the ref keyword to resolve  
};  
```  
