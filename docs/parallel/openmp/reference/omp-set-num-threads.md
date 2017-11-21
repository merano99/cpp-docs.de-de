---
title: "omp_set_num_threads | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "omp_set_num_threads"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "omp_set_num_threads OpenMP function"
ms.assetid: dae0bf3f-cd7a-4413-89de-6149ac1f4fa7
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# omp_set_num_threads
[!INCLUDE[vs2017banner](../../../assembler/inline/includes/vs2017banner.md)]

Legt die Anzahl der Threads in den folgenden Bereichen paralleler fest, sofern kein Überschreiben durch eine [num\_threads](../../../parallel/openmp/reference/num-threads.md)\-Klausel.  
  
## Syntax  
  
```  
void omp_set_num_threads(  
   int num_threads  
);  
```  
  
## Hinweise  
 Hierbei ist:  
  
 `num_threads`  
 Die Anzahl von Threads im parallelen Bereich.  
  
## Hinweise  
 Weitere Informationen finden Sie unter [3.1.1 omp\_set\_num\_threads Function](../../../parallel/openmp/3-1-1-omp-set-num-threads-function.md).  
  
## Beispiel  
 Weitere Informationen finden Sie unter [omp\_get\_num\_threads](../../../parallel/openmp/reference/omp-get-num-threads.md) als ein Beispiel für die Verwendung von `omp_set_num_threads`.  
  
## Siehe auch  
 [Functions](../../../parallel/openmp/reference/openmp-functions.md)