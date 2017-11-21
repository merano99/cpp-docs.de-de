---
title: "make_heap (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::make_heap"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "make_heap-Funktion [STL/CLR]"
ms.assetid: bc1bed28-7a26-4540-901d-5584cd117ea1
caps.latest.revision: 4
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 4
---
# make_heap (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Konvertiert Elemente von einem angegebenen Bereichs in einen Heap, in dem das erste Element ist und für das Element, das ein Sortierungskriterium möglicherweise mit einem binären Prädikat angegeben wird.  
  
## Syntax  
  
```  
template<class _RanIt> inline  
    void make_heap(_RanIt _First, _RanIt _Last);  
template<class _RanIt, class _Pr> inline  
    void make_heap(_RanIt _First, _RanIt _Last, _Pr _Pred);  
```  
  
## Hinweise  
 Diese Funktion verhält sich genauso wie die STL\-Funktion `make_heap`.  Weitere Informationen finden Sie unter [make\_heap](../Topic/make_heap.md).  
  
## Anforderungen  
 **Header:** \<cliext\/Algorithmus\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [algorithm](../dotnet/algorithm-stl-clr.md)