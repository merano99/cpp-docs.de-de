---
title: ATL-Connection Point-Klassen | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- CFirePropNotifyEvent class, connection point classes
- connection points [C++], ATL classes
- ATL, connection points
- CComDynamicUnkArray class, connection point classes
- CFirePropNotifyEvent class
- CComUnkArray class, connection point classes
ms.assetid: 9582ba71-7ace-4df4-9c9b-1b0636953efc
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: ec0a17c47b3a2b30f1f2a2a73a0633ffa321b2a1
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="atl-connection-point-classes"></a>ATL-Connection Point-Klassen
ATL verwendet die folgenden Klassen, um die Verbindungspunkte unterstützen:  
  
-   [IConnectionPointImpl](../atl/reference/iconnectionpointimpl-class.md) implementiert einen Verbindungspunkt. Die IID der Ausgangsschnittstelle, die es darstellt, wird als Vorlagenparameter übergeben.  
  
-   [IConnectionPointContainerImpl](../atl/reference/iconnectionpointcontainerimpl-class.md) Container für die Verbindung implementiert und verwaltet die Liste der `IConnectionPointImpl` Objekte.  
  
-   [IPropertyNotifySinkCP](../atl/reference/ipropertynotifysinkcp-class.md) implementiert, ein Verbindung Punkt, der [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) Schnittstelle.  
  
-   [CComDynamicUnkArray](../atl/reference/ccomdynamicunkarray-class.md) verwaltet eine beliebige Anzahl von Verbindungen zwischen dem Verbindungspunkt und seine senken.  
  
-   [CComUnkArray](../atl/reference/ccomunkarray-class.md) verwaltet eine vordefinierte Anzahl von Verbindungen, wie durch den Vorlagenparameter angegeben.  
  
-   [CFirePropNotifyEvent](../atl/reference/cfirepropnotifyevent-class.md) benachrichtigt der Senke eines Clients, die die Eigenschaft eines Objekts geändert wurde oder zu ändern.  
  
-   [IDispEventImpl](../atl/reference/idispeventimpl-class.md) bietet Unterstützung für Verbindungspunkte für ein ATL-COM-Objekt. Diese Verbindungspunkte werden mit einer ereigniszuordnung Senke zugeordnet, die von COM-Objekt bereitgestellt wird.  
  
-   [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) funktioniert in Verbindung mit der Ereignis-Sink-Zuordnung in die Klasse, um Ereignisse weiterzuleiten, an die entsprechenden Handler-Funktion.  
  
## <a name="see-also"></a>Siehe auch  
 [Verbindungspunkt](../atl/atl-connection-points.md)
