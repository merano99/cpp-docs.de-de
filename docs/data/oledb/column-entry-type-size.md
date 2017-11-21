---
title: "COLUMN_ENTRY_TYPE_SIZE | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "COLUMN_ENTRY_TYPE_SIZE"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "COLUMN_ENTRY_TYPE_SIZE-Marko"
ms.assetid: d8b169e8-af22-464b-8cb3-eaa346f7a739
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# COLUMN_ENTRY_TYPE_SIZE
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Stellt eine Bindung zur spezifischen Spalte in der Datenbank dar.  Unterstützung Parameter `type` und `size`.  
  
## Syntax  
  
```  
  
COLUMN_ENTRY_TYPE_SIZE(  
nOrdinal  
,   
wType  
,   
nLength  
,   
data  
 )  
  
```  
  
#### Parameter  
 `nOrdinal`  
 \[in\] Spaltennummer.  
  
 `wType`  
 \[in\] Datentyp des Spalteneintrags.  
  
 `nLength`  
 \[in\] Größe des Spalteneintrags in Bytes.  
  
 `data`  
 \[in\] der entsprechenden Datenmember im Benutzerdatensatz.  
  
## Hinweise  
 Dieses Makro ist eine besondere Variante des Makros [COLUMN\_ENTRY](../../data/oledb/column-entry.md), d das Angeben der Datengröße und Typ bereitstellt.  
  
## Anforderungen  
 **Header:** atldbcli.h  
  
## Siehe auch  
 [Makros und globale Funktionen für OLE\-Consumervorlagen](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)   
 [BEGIN\_COLUMN\_MAP](../../data/oledb/begin-column-map.md)   
 [END\_COLUMN\_MAP](../../data/oledb/end-column-map.md)