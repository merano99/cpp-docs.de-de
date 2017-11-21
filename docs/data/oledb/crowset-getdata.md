---
title: "CRowset::GetData | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CRowset<TAccessor>::GetData"
  - "ATL::CRowset<TAccessor>::GetData"
  - "ATL::CRowset::GetData"
  - "ATL.CRowset<TAccessor>.GetData"
  - "CRowset<TAccessor>.GetData"
  - "CRowset::GetData"
  - "CRowset.GetData"
  - "ATL.CRowset.GetData"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GetData-Methode [OLE DB]"
ms.assetid: 1e0347b5-3e24-4ff8-a790-839616c1522f
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# CRowset::GetData
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Ruft Daten von der Zeilenkopie des Rowsets ab.  
  
## Syntax  
  
```  
  
      HRESULT GetData( ) throw( );   
HRESULT GetData(   
   int nAccessor    
) throw( );  
```  
  
#### Parameter  
 `nAccessor`  
 \[in\] Die \(NullOffset\) Indexnummer Accessor zur Verwendung für das Zugreifen auf die Daten.  
  
## Rückgabewert  
 Standard\- `HRESULT`.  
  
## Hinweise  
 Wenn Sie einem Accessor angeben, ob in der kein [BEGIN\_ACCESSOR](../../data/oledb/begin-accessor.md) ist, verwenden Sie diese Methode, um die Daten explizit abrufen, indem Sie die Accessornummer übergeben.  
  
## Anforderungen  
 **Header:** atldbcli.h  
  
## Siehe auch  
 [CRowset\-Klasse](../../data/oledb/crowset-class.md)