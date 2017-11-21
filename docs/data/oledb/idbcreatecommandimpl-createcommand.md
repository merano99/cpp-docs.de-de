---
title: "IDBCreateCommandImpl::CreateCommand | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDBCreateCommandImpl.CreateCommand"
  - "CreateCommand"
  - "IDBCreateCommandImpl::CreateCommand"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CreateCommand-Methode"
ms.assetid: 50ffbf8b-2c07-4bcb-96c5-ffce4519c7f7
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# IDBCreateCommandImpl::CreateCommand
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Erstellt einen neuen Befehl und die angeforderte Schnittstelle zurück.  
  
## Syntax  
  
```  
  
      STDMETHOD(CreateCommand)(   
   IUnknown * pUnkOuter,   
   REFIID riid,   
   IUnknown ** ppvCommand    
);  
```  
  
#### Parameter  
 Siehe [IDBCreateCommand::CreateCommand](https://msdn.microsoft.com/en-us/library/ms709772.aspx) in der *OLE* DB\-Programmierreferenz.  
  
 Einige Parameter entsprechen *den OLE DB Programmer's Reference\-Parametern* von verschiedenen Namen, die in **IDBCreateCommand::CreateCommand** beschrieben werden:  
  
|OLE DB\-Vorlagen\-Parameter|*OLE DB Programmer's Reference\-*\-Parameter|  
|---------------------------------|--------------------------------------------------|  
|*ppvCommand*|*ppCommand*|  
  
## Anforderungen  
 **Header:** atldb.h  
  
## Siehe auch  
 [IDBCreateCommandImpl\-Klasse](../../data/oledb/idbcreatecommandimpl-class.md)