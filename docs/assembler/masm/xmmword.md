---
title: "XMMWORD | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "XMMWORD"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "XMMWORD directive"
ms.assetid: 18026d32-5cab-403e-ad7e-382fb41aa9b8
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# XMMWORD
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Wird für Multimedia Operanden des 128\-Bits mit MMX und XTM \(SSE\) \- Anweisungen.  
  
## Syntax  
  
```  
XMMWORD  
```  
  
## Hinweise  
 `XMMWORD` muss den gleichen Typ wie [\_\_m128](../../cpp/m128.md)darzustellen.  
  
## Beispiel  
  
```  
movdqa   xmm0, xmmword ptr [ebx]  
```