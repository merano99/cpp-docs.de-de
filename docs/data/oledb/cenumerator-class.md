---
title: "CEnumerator-Klasse | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CEnumerator"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CEnumerator-Klasse"
ms.assetid: 25805f1b-26e3-402f-af83-1b5fe5ddebf7
caps.latest.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# CEnumerator-Klasse
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Verwendet ein OLE DB\-Enumeratorobjekt, das die [ISourcesRowset](https://msdn.microsoft.com/en-us/library/ms715969.aspx)\-Schnittstelle verfügbar macht, um einem Rowset zurückgegeben, das alle Datenquellen und Enumeratoren beschreibt.  
  
## Syntax  
  
```  
class CEnumerator :   
   public CAccessorRowset< CAccessor <CEnumeratorAccessor >>  
```  
  
## Member  
  
### Methoden  
  
|||  
|-|-|  
|[Find](../../data/oledb/cenumerator-find.md)|Suchen von der verfügbaren Anbieter \(Datenquellen\) nach einem mit dem angegebenen Namen zu finden.|  
|[GetMoniker](../../data/oledb/cenumerator-getmoniker.md)|Ruft die `IMoniker`\-Schnittstelle für den aktuellen Datensatz ab.|  
|[Öffnen](../../data/oledb/cenumerator-open.md)|Öffnet den Enumerator.|  
  
## Hinweise  
 Sie können die **ISourcesRowset** Daten aus dieser Klasse indirekt abrufen.  
  
## Anforderungen  
 **Header:** atldbcli.h  
  
## Siehe auch  
 [DBViewer](../../top/visual-cpp-samples.md)   
 [OLE DB\-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [Referenz der OLE DB\-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-reference.md)