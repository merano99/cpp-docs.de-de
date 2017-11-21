---
title: "__inwordstring | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "__inwordstring"
  - "__inwordstring_cpp"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "__inwordstring intrinsic"
  - "rep insw-Anweisung"
ms.assetid: 6de37939-017a-4740-9e3d-7de78a30daba
caps.latest.revision: 11
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 11
---
# __inwordstring
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Microsoft\-spezifisch**  
  
 Liest Daten aus dem angegebenen Port mit der `rep insw`\-Anweisung.  
  
## Syntax  
  
```  
void __inwordstring(  
   unsigned short Port,  
   unsigned short* Buffer,  
   unsigned long Count  
);  
```  
  
#### Parameter  
 \[in\] `Port`  
 Der zum Lesen von Port.  
  
 \[out\] `Buffer`  
 Die Daten, die vom Port gelesenen, wird hier geschrieben.  
  
 \[in\] `Count`  
 Die Anzahl von Wörtern von Daten gelesen werden soll.  
  
## Anforderungen  
  
|Intrinsisch|Architektur|  
|-----------------|-----------------|  
|`__inwordstring`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **Headerdatei** \<intrin.h\>  
  
## Hinweise  
 Diese Routine ist als systeminterne Funktion nur verfügbar.  
  
## Microsoft ENDES bestimmten  
  
## Siehe auch  
 [Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)