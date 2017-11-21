---
title: Compilerfehler C2289 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2289
dev_langs: C++
helpviewer_keywords: C2289
ms.assetid: cb41a29e-1b06-47dc-bfce-8d73bd63a0df
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 6c771780ad3bbaefd51be10c9ff1454127f8439b
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2289"></a>Compilerfehler C2289
Der gleiche Typqualifizierer wurde mehrmals verwendet  
  
 Ein Typqualifizierer (`const`, `volatile`, `signed`oder `unsigned`) wird in einer Typdeklaration oder -definition mehrfach verwendet. Dabei wird bei Einhaltung der ANSI-Kompatibilität (**/Za**) eine Fehlermeldung ausgegeben.  
  
 Im folgenden Beispiel wird C2286 generiert:  
  
```  
// C2289.cpp  
// compile with: /Za /c  
volatile volatile int i;   // C2289  
volatile int j;   // OK  
```