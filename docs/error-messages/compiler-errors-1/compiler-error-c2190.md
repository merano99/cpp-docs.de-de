---
title: Compilerfehler C2190 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2190
dev_langs:
- C++
helpviewer_keywords:
- C2190
ms.assetid: 34e15f85-d979-4948-80fc-46c414508a70
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: d004d5a80e6907695f742faf6573c348662a479b
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2190"></a>Compilerfehler C2190
erste Parameterliste länger als zweite  
  
 Eine C-Funktion wurde ein zweites Mal mit einer kürzeren Parameterliste deklariert. C# unterstützt keine überladene Funktionen.  
  
 Im folgende Beispiel wird C2190 generiert:  
  
```  
// C2190.c  
// compile with: /Za /c  
void func( int, float );  
void func( int  );   // C2190, different parameter list  
void func2( int  );   // OK  
```