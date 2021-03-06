---
title: IRowsetNotifyCP-Klasse
ms.date: 11/04/2016
f1_keywords:
- IRowsetNotifyCP
- Fire_OnFieldChange
- ATL::IRowsetNotifyCP::Fire_OnFieldChange
- ATL.IRowsetNotifyCP.Fire_OnFieldChange
- IRowsetNotifyCP.Fire_OnFieldChange
- IRowsetNotifyCP::Fire_OnFieldChange
- IRowsetNotifyCP.Fire_OnRowChange
- ATL.IRowsetNotifyCP.Fire_OnRowChange
- Fire_OnRowChange
- ATL::IRowsetNotifyCP::Fire_OnRowChange
- IRowsetNotifyCP::Fire_OnRowChange
- Fire_OnRowsetChange
- IRowsetNotifyCP::Fire_OnRowsetChange
- IRowsetNotifyCP.Fire_OnRowsetChange
- ATL::IRowsetNotifyCP::Fire_OnRowsetChange
- ATL.IRowsetNotifyCP.Fire_OnRowsetChange
helpviewer_keywords:
- IRowsetNotifyCP class
- Fire_OnFieldChange method
- Fire_OnRowChange method
- Fire_OnRowsetChange method
ms.assetid: ccef402b-94a0-4c2e-9a13-7e854ef82390
ms.openlocfilehash: 119cc79cf0f3ed5784e1b3b291fce52f06695d36
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556282"
---
# <a name="irowsetnotifycp-class"></a>IRowsetNotifyCP-Klasse

Die Website für die Verbindungspunkt-Schnittstelle implementiert [IRowsetNotify](https://docs.microsoft.com/previous-versions/windows/desktop/ms712959(v=vs.85)).

## <a name="syntax"></a>Syntax

```cpp
template <class T, class ReentrantEventSync = CComSharedMutex>
class IRowsetNotifyCP :
   public IConnectionPointImpl<
      T,
      piid = &__uuidof(IRowsetNotify),
      CComDynamicUnkArray DynamicUnkArray>,
   public ReentrantEventSync
```

### <a name="parameters"></a>Parameter

*T*<br/>
Eine abgeleitete Klasse `IRowsetNotifyCP`.

*ReentrantEventSync*<br/>
Ein Mutex-Klasse, die Eintrittsinvarianz unterstützt (die Standardeinstellung ist `CComSharedMutex`). Ein Mutex ist ein Synchronisierungsobjekt, das Threads den einander ausschließenden Zugriff auf eine Ressource ermöglicht.

*piid*<br/>
Ein ID-Schnittstellenzeiger (`IID*`) für eine `IRowsetNotify` Verbindungspunkt-Schnittstelle. Der Standardwert ist `&__uuidof(IRowsetNotify)`.

*DynamicUnkArray*<br/>
Ein Array vom Typ [CComDynamicUnkArray](../../atl/reference/ccomdynamicunkarray-class.md), d.h. ein dynamisch zugeordnetes Array aus `IUnknown` sink-Schnittstellen Zeigern auf dem Client.

## <a name="requirements"></a>Anforderungen

**Header:** „atldb.h“

## <a name="members"></a>Member

### <a name="methods"></a>Methoden

|||
|-|-|
|[Fire_OnFieldChange](#onfieldchange)|Benachrichtigt den Consumer über eine Änderung an den Wert einer Spalte.|
|[Fire_OnRowChange](#onrowchange)|Benachrichtigt den Consumer über eine Änderung, die Auswirkungen auf die Zeilen.|
|[Fire_OnRowsetChange](#onrowsetchange)|Benachrichtigt den Consumer über eine Änderung, die Auswirkungen auf das gesamte Rowset.|

## <a name="remarks"></a>Hinweise

`IRowsetNotifyCP` broadcast-implementiert Funktionen, um den Listener auf dem Verbindungspunkt empfehlen `IID_IRowsetNotify` von Änderungen an den Inhalt des Rowsets.

Beachten Sie, dass Sie auch implementieren registrieren müssen `IRowsetNotify` vom Consumer (auch bekannt als "Senke" genannt) mit [IRowsetNotifyImpl](../../data/oledb/irowsetnotifyimpl-class.md) , damit der Consumer mit Benachrichtigungen behandeln kann. Finden Sie unter [empfangen von Benachrichtigungen](../../data/oledb/receiving-notifications.md) zur Implementierung der vom Consumer der Verbindungspunkt-Schnittstelle.

Ausführliche Informationen zum Implementieren von Benachrichtigungen finden Sie unter "Unterstützen von Benachrichtigungen" in [Erstellen eines aktualisierbaren Anbieters](../../data/oledb/creating-an-updatable-provider.md).

## <a name="onfieldchange"></a> IRowsetNotifyCP:: Fire_onfieldchange

Überträgt ein [OnFieldChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms715961(v=vs.85)) Ereignis benachrichtigt Kunden über eine Änderung an den Wert einer Spalte.

### <a name="syntax"></a>Syntax

```cpp
HRESULT Fire_OnFieldChange(IRowset* pRowset,
   HROW hRow,
   DBORDINAL cColumns,
   DBORDINAL* rgColumns,
   DBREASON eReason,
   DBEVENTPHASE ePhase,
   BOOL fCantDeny);
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [IRowsetNotify::OnFieldChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms715961(v=vs.85)) in die *OLE DB-Programmierreferenz*.

## <a name="onrowchange"></a> IRowsetNotifyCP:: Fire_onrowchange

Überträgt ein [OnRowChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms722694(v=vs.85)) Ereignis an alle Listener für den Verbindungspunkt `IID_IRowsetNotify` benachrichtigen Kunden über eine Änderung, die Auswirkungen auf die Zeilen.

### <a name="syntax"></a>Syntax

```cpp
HRESULT Fire_OnRowChange(IRowset* pRowset,
   DBCOUNTITEM cRows,
   const HROW rghRows[],
   DBREASON eReason,
   DBEVENTPHASE ePhase,
   BOOL fCantDeny);
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [IRowsetNotify::OnRowChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms722694(v=vs.85)) in die *OLE DB-Programmierreferenz*.

## <a name="onrowsetchange"></a> IRowsetNotifyCP:: Fire_onrowsetchange

Überträgt ein [OnRowsetChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms722669(v=vs.85)) Ereignis an alle Listener für den Verbindungspunkt `IID_IRowsetNotify` benachrichtigen Kunden über eine Änderung, die Auswirkungen auf das gesamte Rowset.

### <a name="syntax"></a>Syntax

```cpp
HRESULT Fire_OnRowsetChange(IRowset* pRowset,
   DBREASON eReason,
   DBEVENTPHASE ePhase,
   BOOL fCantDeny);
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [IRowsetNotify::OnRowsetChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms722669(v=vs.85)) in die *OLE DB-Programmierreferenz*.

## <a name="see-also"></a>Siehe auch

[OLE DB-Anbietervorlagen](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[Architektur von OLE DB-Anbietervorlagen](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
[Benachrichtigungen (COM)](/windows/desktop/com/notifications)<br/>
[BEGIN_CONNECTION_POINT_MAP](../../atl/reference/connection-point-macros.md#begin_connection_point_map)<br/>
[END_CONNECTION_POINT_MAP](../../atl/reference/connection-point-macros.md#end_connection_point_map)<br/>
[CONNECTION_POINT_ENTRY](../../atl/reference/connection-point-macros.md#connection_point_entry)<br/>
[Erstellen eines aktualisierbaren Anbieters](../../data/oledb/creating-an-updatable-provider.md)