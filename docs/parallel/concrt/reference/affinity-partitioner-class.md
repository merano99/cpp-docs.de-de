---
title: Affinity_partitioner-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- affinity_partitioner
- PPL/concurrency::affinity_partitioner
- PPL/concurrency::affinity_partitioner::affinity_partitioner
dev_langs:
- C++
helpviewer_keywords:
- affinity_partitioner class
ms.assetid: 31bf7bb1-bd01-491c-9760-d9d60edfccad
caps.latest.revision: 9
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 5faef5bd1be6cc02d6614a6f6193c74167a8ff23
ms.openlocfilehash: 066557d522bc18237ccc484be8b59dc53b7e2905
ms.contentlocale: de-de
ms.lasthandoff: 03/17/2017

---
# <a name="affinitypartitioner-class"></a>affinity_partitioner-Klasse
Die `affinity_partitioner`-Klasse ist der `static_partitioner`-Klasse ähnlich, allerdings wird die Cacheaffinität dank der Auswahl, den Arbeitsthreads Unterbereiche zuzuordnen, verbessert. Sie kann die Leistung, bei erneutem Ausführen einer Schleife über dem gleichen Dataset, und wenn die Daten im Cache gespeichert werden können, erheblich verbessern. Beachten Sie, dass das gleiche `affinity_partitioner`-Objekt mit nachfolgenden Iterationen einer parallelen Schleife verwendet werden muss, die für ein bestimmtes Dataset ausgeführt wird, um vom Datenort zu profitieren.  
  
## <a name="syntax"></a>Syntax  
  
```
class affinity_partitioner;
```  
  
## <a name="members"></a>Mitglieder  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[affinity_partitioner](#ctor)|Erstellt ein `affinity_partitioner`-Objekt.|  
|[~ Affinity_partitioner-Destruktor](#dtor)|Zerstört ein `affinity_partitioner` Objekt.|  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 `affinity_partitioner`  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** ppl.h  
  
 **Namespace:** Parallelität  
  
##  <a name="dtor"></a>~ Affinity_partitioner 

 Zerstört ein `affinity_partitioner` Objekt.  
  
```
~affinity_partitioner();
```  
  
##  <a name="ctor"></a>affinity_partitioner 

 Erstellt ein `affinity_partitioner`-Objekt.  
  
```
affinity_partitioner();
```  
  
## <a name="see-also"></a>Siehe auch  
 [Concurrency-Namespace](concurrency-namespace.md)
