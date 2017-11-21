---
title: Compilerfehler C3213 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3213
dev_langs: C++
helpviewer_keywords: C3213
ms.assetid: 1f079e36-b3e9-40f8-8e95-08eeba3adc82
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 68121ff469ac0018575b9db0b31ba3103a69e93c
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3213"></a>Compilerfehler C3213
Die Basisklasse 'base_type' hat eine stärkere Zugriffsbeschränkung als 'derived_type'  
  
 Ein Typ, der von einer Assembly aus sichtbar ist, muss öffentlich sichtbare Basisklassen verwenden.  
  
 Im folgenden Beispiel wird C3213 generiert:  
  
```  
// C3213.cpp  
// compile with: /clr  
private ref struct privateG {  
public:  
   int i;  
};  
  
public ref struct publicG {  
public:  
   int i;  
};  
  
public ref struct V : public privateG {   // C3213  
public:  
   int j;  
};  
  
public ref struct W: public publicG {   // OK  
public:  
   int j;  
};  
```