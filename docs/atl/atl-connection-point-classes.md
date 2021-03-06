---
title: ATL-Connection Point-Klassen
ms.date: 11/04/2016
helpviewer_keywords:
- CFirePropNotifyEvent class, connection point classes
- connection points [C++], ATL classes
- ATL, connection points
- CComDynamicUnkArray class, connection point classes
- CFirePropNotifyEvent class
- CComUnkArray class, connection point classes
ms.assetid: 9582ba71-7ace-4df4-9c9b-1b0636953efc
ms.openlocfilehash: c4b2a9b295997c809acf9b037cd5f124f0752c3b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50439376"
---
# <a name="atl-connection-point-classes"></a>ATL-Connection Point-Klassen

ATL verwendet die folgenden Klassen, um die Verbindungspunkte unterstützen:

- [IConnectionPointImpl](../atl/reference/iconnectionpointimpl-class.md) implementiert einen Verbindungspunkt. Die IID der Ausgangsschnittstelle, die es darstellt, die als Vorlagenparameter übergeben wird.

- [IConnectionPointContainerImpl](../atl/reference/iconnectionpointcontainerimpl-class.md) der Verbindungspunktcontainer implementiert und verwaltet die Liste der `IConnectionPointImpl` Objekte.

- [IPropertyNotifySinkCP](../atl/reference/ipropertynotifysinkcp-class.md) implementiert ein Connection Point, die [IPropertyNotifySink](/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink) Schnittstelle.

- [CComDynamicUnkArray](../atl/reference/ccomdynamicunkarray-class.md) verwaltet eine beliebige Anzahl von Verbindungen zwischen dem Verbindungspunkt und die senken.

- [CComUnkArray](../atl/reference/ccomunkarray-class.md) verwaltet eine vordefinierte Anzahl an Verbindungen, die vom Vorlagenparameter angegeben.

- [CFirePropNotifyEvent](../atl/reference/cfirepropnotifyevent-class.md) benachrichtigt der Senke eines Clients, die die Eigenschaft eines Objekts geändert hat oder zu ändern.

- [IDispEventImpl](../atl/reference/idispeventimpl-class.md) bietet Unterstützung für die Verbindungspunkte für ein ATL-COM-Objekt. Mit einer Ereignis-Senke-Karte, die von COM-Objekts bereitgestellt wird, werden diese Verbindungspunkte zugeordnet.

- [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) funktioniert in Verbindung mit der Ereignis-Sink-Zuordnung in der Klasse zum Weiterleiten von Ereignissen an die entsprechenden Handler-Funktion.

## <a name="see-also"></a>Siehe auch

[Verbindungspunkt](../atl/atl-connection-points.md)

