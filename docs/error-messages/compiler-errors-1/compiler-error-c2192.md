---
title: Compilerfehler C2192 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2192
dev_langs: C++
helpviewer_keywords: C2192
ms.assetid: a147197e-e72d-4620-939b-f9e08d7c7c12
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: c56dae7438c8c8dd7d17332f65b5c32aff16db39
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2192"></a>Compilerfehler C2192
Parameter 'Number'-Deklaration verschiedene  
  
 Eine C-Funktion wurde ein zweites Mal mit einer anderen Parameterliste deklariert. C# unterstützt keine überladene Funktionen.  
  
 Im folgende Beispiel wird C2192 generiert:  
  
```  
// C2192.c  
// compile with: /Za /c  
void func( float, int );  
void func( int, float );   // C2192, different parameter list  
void func2( int, float );   // OK  
```