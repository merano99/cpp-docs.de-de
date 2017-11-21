---
title: "Erweitern des einfachen schreibgeschützten Anbieters | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- read-only poviders [C++]
- IRowsetLocate class
- IRowsetLocate class, adding to OLE DB template providers
- simple read-only poviders [C++]
ms.assetid: cba0e09f-44c1-41c1-9456-332aa13dc158
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 30b87ecae6f479c912c937fb2ce23e1f9dc98da3
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="enhancing-the-simple-read-only-provider"></a>Erweitern des einfachen schreibgeschützten Anbieters
In diesem Abschnitt wird gezeigt, wie zur Verbesserung der [einfachen schreibgeschützten Anbieters](../../data/oledb/implementing-the-simple-read-only-provider.md) im vorherigen Abschnitt erstellt haben. `IRowsetLocateImpl`erstellt eine Implementierung für die `IRowsetLocate` Schnittstelle und fügt lesezeichenunterstützung für Sie.  
  
 Wenn Sie einen funktionierende-Anbieter verfügen, empfiehlt es sich um stellen die Anbieter-Updates, Verarbeiten von Transaktionen oder verbessern die Leistung des Algorithmus Abrufen von Zeilen verbessern. Die meisten Anbieter-Verbesserungen umfassen das Hinzufügen einer Schnittstelle zu einem vorhandenen COM-Objekt.  
  
 Im Beispiel in den folgenden Themen wird den Mechanismus zum Abrufen von Zeilen, indem die `IRowsetLocate` -Schnittstelle `CAgentRowset`. In den Themen wird wie auf:  
  
-   [Vornehmen von "RMyProviderRowset" IRowsetLocate erben](../../data/oledb/modifying-the-inheritance-of-rmyproviderrowset.md).  
  
-   [Dynamisches Festlegen der an den Consumer zurückgegebenen Spalten](../../data/oledb/dynamically-determining-columns-returned-to-the-consumer.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Erstellen eines einfachen schreibgeschützten Anbieters](../../data/oledb/creating-a-simple-read-only-provider.md)