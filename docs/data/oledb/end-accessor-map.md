---
title: "END_ACCESSOR_MAP | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "END_ACCESSOR_MAP"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "END_ACCESSOR_MAP-Makro"
ms.assetid: ede813c7-46c9-48a6-aa1a-8ebf38e92023
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# END_ACCESSOR_MAP
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Markiert das Ende der Accessorzuordnungseinträge.  
  
## Syntax  
  
```  
  
END_ACCESSOR_MAP( )  
  
```  
  
## Hinweise  
 Für mehrere Accessoren für ein Rowset, müssen Sie `BEGIN_ACCESSOR_MAP` angeben und das Makro `BEGIN_ACCESSOR` für jeden einzelnen Accessor verwenden.  Das Makro `BEGIN_ACCESSOR` wird mit dem Makro `END_ACCESSOR` abgeschlossen.  Das Makro `BEGIN_ACCESSOR_MAP` wird mit dem Makro `END_ACCESSOR_MAP` abgeschlossen.  
  
## Beispiel  
 Siehe [BEGIN\_ACCESSOR\_MAP](../../data/oledb/begin-accessor-map.md).  
  
## Anforderungen  
 **Header:** atldbcli.h  
  
## Siehe auch  
 [Makros und globale Funktionen für OLE\-Consumervorlagen](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)   
 [BEGIN\_ACCESSOR\_MAP](../../data/oledb/begin-accessor-map.md)   
 [BEGIN\_ACCESSOR](../../data/oledb/begin-accessor.md)