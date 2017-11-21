---
title: "Kumulative Abh&#228;ngigkeiten | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "kumulative Abhängigkeiten"
  - "Kumulative Abhängigkeiten in NMAKE"
  - "Abhängigkeiten"
ms.assetid: fa6dd777-80b8-437d-87a7-aec0ed818a49
caps.latest.revision: 11
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 11
---
# Kumulative Abh&#228;ngigkeiten
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Abhängigkeiten sind in einem Beschreibungsblock kumulativ, wenn ein Ziel wiederholt wird.  
  
 Legen Sie diesen z. B. Regeln,  
  
```Output  
bounce.exe : jump.obj  
bounce.exe : up.obj  
   echo Building bounce.exe...  
```  
  
 wird folgendermaßen ausgewertet:  
  
```Output  
bounce.exe : jump.obj up.obj  
   echo Building bounce.exe...  
```  
  
 Mehrere Ziele in mehreren Abhängigkeitszeilen in einer einzelnen Beschreibungsblöcken werden ausgewertet, als ob jedes in einer separaten Beschreibungsblöcken angegeben wurden, Ziele, die nicht in der letzten Abhängigkeitszeile verwenden jedoch kein Befehlsblock. NMAKE versucht, eine Rückschlussregel für diese Ziele zu verwenden.  
  
 Legen Sie diesen z. B. Regeln,  
  
```Output  
leap.exe bounce.exe : jump.obj  
bounce.exe climb.exe : up.obj  
   echo Building bounce.exe...  
```  
  
 wird folgendermaßen ausgewertet:  
  
```Output  
  
leap.exe : jump.obj  
# invokes an inference rule  
bounce.exe : jump.obj up.obj  
   echo Building bounce.exe...  
climb.exe : up.obj  
   echo Building bounce.exe...  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Ziele](../build/targets.md)