---
title: 'CUtlProps:: Oninterfacerequested | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CUtlProps
dev_langs: C++
helpviewer_keywords: OnInterfaceRequested method
ms.assetid: a5e1a879-cff3-4e01-b902-2249a152984f
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 860870628d8558ad252657c06d90f195fd707eb8
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="cutlpropsoninterfacerequested"></a>CUtlProps::OnInterfaceRequested
Verarbeitet Anforderungen für eine optionale Schnittstelle, wenn ein Consumer eine Methode eines Objekts erstellen Schnittstellen aufruft.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      virtual HRESULT CUtlPropsBase::OnInterfaceRequested(  
   REFIID riid  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `riid`  
 [in] Die IID für die angeforderte Schnittstelle. Weitere Informationen finden Sie unter der Beschreibung der der `riid` Parameter `ICommand::Execute` in der *OLE DB Programmer's Reference* (in der *MDAC SDK*).  
  
## <a name="remarks"></a>Hinweise  
 **OnInterfaceRequested** Consumeranforderungen für eine optionale Schnittstelle behandelt, wenn ein Consumer eine Methode eines Objekts erstellen Schnittstellen aufruft (z. B. **IDBCreateSession**, **IDBCreateCommand**, `IOpenRowset`, oder `ICommand`). Die entsprechende OLE DB-Eigenschaft für die angeforderte Schnittstelle festgelegt. Angenommen, fordert der Consumer **IID_IRowsetLocate**, **OnInterfaceRequested** legt die **DBPROP_IRowsetLocate** Schnittstelle. Auf diese Weise verwaltet den richtigen Status während der rowseterstellung.  
  
 Diese Methode wird aufgerufen, wenn der Consumer ruft **IOpenRowset:: OPENROWSET** oder `ICommand::Execute`.  
  
 Wenn ein Consumer ein Objekt öffnet, und eine optionale Schnittstelle fordert, sollte der Anbieter die Eigenschaft, die die Schnittstelle zugeordnet festlegen `VARIANT_TRUE`. Die Eigenschaftenspezifisch-Verarbeitung ermöglicht **OnInterfaceRequested** wird aufgerufen, bevor des Anbieters **Execute** -Methode aufgerufen wird. Standardmäßig **OnInterfaceRequested** behandelt die folgenden Schnittstellen:  
  
-   `IRowsetLocate`  
  
-   `IRowsetChange`  
  
-   `IRowsetUpdate`  
  
-   **IConnectionPointContainer**  
  
-   `IRowsetScroll`  
  
 Wenn Sie andere Schnittstellen behandeln möchten, überschreiben Sie diese Funktion in die Datenklasse Quelle, Session, Befehls- oder Rowset Prozess Funktionen. Die Außerkraftsetzung sollte die normalen Set/Get Eigenschaften Schnittstellen, um sicherzustellen, dass die Eigenschaften auch alle verketteten Eigenschaften festlegen, durchlaufen (finden Sie unter [OnPropertyChanged](../../data/oledb/cutlprops-onpropertychanged.md)).  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** „atldb.h“  
  
## <a name="see-also"></a>Siehe auch  
 [CUtlProps-Klasse](../../data/oledb/cutlprops-class.md)