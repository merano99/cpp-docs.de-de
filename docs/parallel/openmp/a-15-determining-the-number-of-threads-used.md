---
title: Bestimmen der Anzahl der verwendeten Threads A.15 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 026bb59a-f668-40db-a7cb-69a1bae83d2d
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 50dcc445a88350dcafb4d37039ff09d98a8c5581
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="a15---determining-the-number-of-threads-used"></a>A.15   Ermitteln der Anzahl von verwendeten Threads
Betrachten Sie das folgende Beispiel falsche (für [Abschnitt 3.1.2](../../parallel/openmp/3-1-2-omp-get-num-threads-function.md) auf Seite 37):  
  
```  
np = omp_get_num_threads(); // misplaced   
#pragma omp parallel for schedule(static)  
    for (i=0; i<np; i++)  
        work(i);  
```  
  
 Die `omp_get_num_threads()` Aufrufen gibt 1 zurück in den seriellen Abschnitt des Codes, daher *Np* wird immer im vorherigen Beispiel gleich 1 sein. Um die Anzahl der Threads zu bestimmen, die für den parallelen Bereich bereitgestellt wird, sollte der Aufruf innerhalb des parallelen Bereichs.  
  
 Das folgende Beispiel zeigt, wie Sie dieses Programm zu schreiben, ohne eine Abfrage für die Anzahl der Threads:  
  
```  
#pragma omp parallel private(i)  
{  
    i = omp_get_thread_num();  
    work(i);  
}  
```