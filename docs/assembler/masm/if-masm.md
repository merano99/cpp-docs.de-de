---
title: "IF (MASM) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "if"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "IF directive"
ms.assetid: 82e43712-4f0c-4bf6-90ce-0663e81af707
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# IF (MASM)
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Erteilt Assembly mit *ifstatements,* wenn true \( *expression1*\-Wert ungleich 0 \(null\) oder *elseifstatements* wenn *expression1* ist falsch \(0\) und *expression2* ist true.  
  
## Syntax  
  
```  
  
   IF expression1  
ifstatements  
[[ELSEIF expression2  
   elseifstatements]]  
[[ELSE  
   elsestatements]]  
ENDIF  
```  
  
## Hinweise  
 Die folgenden Direktiven sind für [ELSEIF](../../assembler/masm/elseif-masm.md)ersetzt werden: **ELSEIFB**, **ELSEIFDEF**, **ELSEIFDIF**, **ELSEIFDIFI**, **ELSEIFE**, **ELSEIFIDN**, **ELSEIFIDNI**, **ELSEIFNB**und **ELSEIFNDEF**.  Optional wird *elsestatements zusammengefasst,* wenn der vorherige Ausdruck falsch ist.  Beachten Sie, dass die Ausdrücke in der Montagezeit ausgewertet werden.  
  
## Siehe auch  
 [Directives Reference](../../assembler/masm/directives-reference.md)