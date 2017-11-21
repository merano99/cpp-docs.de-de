---
title: Compilerfehler C2386 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2386
dev_langs: C++
helpviewer_keywords: C2386
ms.assetid: aaaa1284-34a0-4da2-8547-9fcbb559dae0
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 82ed9dc42100e523128bc6a15e6166dda5c02105
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2386"></a>Compilerfehler C2386
'symbol': Ein Symbol mit diesem Namen ist bereits im aktuellen Bereich vorhanden.  
  
 Sie haben versucht, einen Namespacealias zu erstellen, aber der ausgewählte Name ist bereits vorhanden.  
  
 Das folgende Beispiel generiert C2386:  
  
```  
// C2386.cpp  
namespace A {  
   int k;  
}  
  
int i;  
namespace i = A;   // C2386, i already exists  
```