---
title: "raw_dispinterfaces | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "raw_dispinterfaces"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "raw_dispinterfaces-Attribut"
ms.assetid: f762864d-29bf-445b-825a-ba7b29a95409
caps.latest.revision: 4
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 4
---
# raw_dispinterfaces
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**C\+\+\-spezifisch**  
  
 Weist den Compiler an, Wrapperfunktionen auf niedriger Ebene für Disp\-Schnittstellenmethoden und \-eigenschaften zu generieren, die **IDispatch::Invoke** aufrufen und den `HRESULT`\-Fehlercode zurückgeben.  
  
## Syntax  
  
```  
raw_dispinterfaces  
```  
  
## Hinweise  
 Wenn dieses Attribut nicht angegeben wird, werden nur Wrapper auf hoher Ebene generiert, die im Falle eines Fehlers C\+\+\-Ausnahmen auslösen.  
  
 **Ende C\+\+\-spezifisch**  
  
## Siehe auch  
 [\#import\-Attribute](../preprocessor/hash-import-attributes-cpp.md)   
 [\#import\-Direktive](../preprocessor/hash-import-directive-cpp.md)