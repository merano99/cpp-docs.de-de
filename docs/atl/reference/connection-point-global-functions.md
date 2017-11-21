---
title: "Globale Funktionen für Verbindungspunkt | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- atlbase/ATL::AtlAdvise
- atlbase/ATL::AtlUnadvise
- atlbase/ATL::AtlAdviseSinkMap
dev_langs: C++
helpviewer_keywords: connection points [C++], global functions
ms.assetid: bcb4bf50-2155-4e20-b8bb-f2908b03a6e7
caps.latest.revision: "20"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: d4457712cf99a7e5b34632247e027d6765699ac4
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="connection-point-global-functions"></a>Verbindungspunkt globale Funktionen
Diese Funktionen bieten Unterstützung für Verbindungspunkte und sink Maps.  
  
> [!IMPORTANT]
>  In der folgenden Tabelle aufgeführten Funktionen können nicht in Anwendungen verwendet werden, die in der Windows-Runtime ausgeführt werden.  
  
|||  
|-|-|  
|[AtlAdvise](#atladvise)|Erstellt eine Verbindung zwischen dem Verbindungspunkt eines Objekts und der Senke eines Clients.|  
|[AtlUnadvise](#atlunadvise)|Beendet die Verbindung über `AtlAdvise`.|  
|[AtlAdviseSinkMap](#atladvisesinkmap)|Member- oder unadvises Einträge in einer Senke.|  

## <a name="requirements"></a>Anforderungen  
 **Header:** atlbase.h  
   
##  <a name="atladvise"></a>AtlAdvise  
 Erstellt eine Verbindung zwischen dem Verbindungspunkt eines Objekts und der Senke eines Clients.  
  
> [!IMPORTANT]
>  Diese Funktion kann nicht in Anwendungen verwendet werden, die in der Windows-Runtime ausgeführt werden.  
  
```
HRESULT    AtlAdvise(
    IUnknown* pUnkCP,
    IUnknown* pUnk,
    const IID& iid,
    LPDWORD pdw);
```  
  
### <a name="parameters"></a>Parameter  
 `pUnkCP`  
 [in] Ein Zeiger auf die **IUnknown** des Objekts der Client eine Verbindung mit herstellen möchte.  
  
 *pUnk*  
 [in] Ein Zeiger auf des Clients **IUnknown**.  
  
 `iid`  
 [in] Die GUID des Verbindungspunkt. Dies ist normalerweise identisch mit der Ausgangsschnittstelle, von dem Verbindungspunkt verwaltet werden.  
  
 `pdw`  
 [out] Ein Zeiger auf das Cookie, das die Verbindung eindeutig identifiziert.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein standard HRESULT-Wert.  
  
### <a name="remarks"></a>Hinweise  
 Die Senke implementiert die ausgehende Schnittstelle, die durch den Verbindungspunkt unterstützt. Der Client verwendet die `pdw` Cookie beim Entfernen der Verbindung durch Übergabe an [AtlUnadvise](#atlunadvise).  
  
### <a name="example"></a>Beispiel  
 [!code-cpp[NVC_ATL_Windowing#91](../../atl/codesnippet/cpp/connection-point-global-functions_1.cpp)]  
  
##  <a name="atlunadvise"></a>AtlUnadvise  
 Beendet die Verbindung über [AtlAdvise](#atladvise).  
  
> [!IMPORTANT]
>  Diese Funktion kann nicht in Anwendungen verwendet werden, die in der Windows-Runtime ausgeführt werden.  
  
```
HRESULT    AtlUnadvise(
    IUnknown* pUnkCP,
    const IID& iid,
    DWORD dw);
```  
  
### <a name="parameters"></a>Parameter  
 `pUnkCP`  
 [in] Ein Zeiger auf die **IUnknown** des Objekts, das mit der Client verbunden ist.  
  
 `iid`  
 [in] Die GUID des Verbindungspunkt. Dies ist normalerweise identisch mit der Ausgangsschnittstelle, von dem Verbindungspunkt verwaltet werden.  
  
 `dw`  
 [in] Das Cookie, das die Verbindung eindeutig identifiziert.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein standard HRESULT-Wert.  
  
### <a name="example"></a>Beispiel  
 [!code-cpp[NVC_ATL_Windowing#96](../../atl/codesnippet/cpp/connection-point-global-functions_2.cpp)]  
  
##  <a name="atladvisesinkmap"></a>AtlAdviseSinkMap  
 Mit dieser Funktion melden Sie alle Einträge in der Senkereigniszuordnung des Objekts an oder ab.  
  
> [!IMPORTANT]
>  Diese Funktion kann nicht in Anwendungen verwendet werden, die in der Windows-Runtime ausgeführt werden.  
  
```
HRESULT AtlAdviseSinkMap(T* pT, bool bAdvise);
```  
  
### <a name="parameters"></a>Parameter  
 *pT*  
 [in] Ein Zeiger auf das Objekt, das die Sink-Zuordnung enthält.  
  
 `bAdvise`  
 [in] **"true"** Wenn alle Senke Einträge empfohlen werden; **"false"** Wenn alle Senke Einträge unadvised werden sollen.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein standard HRESULT-Wert.  
  
### <a name="example"></a>Beispiel  
 [!code-cpp[NVC_ATL_Windowing#92](../../atl/codesnippet/cpp/connection-point-global-functions_3.h)]  
  
## <a name="see-also"></a>Siehe auch  
 [Funktionen](../../atl/reference/atl-functions.md)   
 [Verbindungspunkt-Makros](../../atl/reference/connection-point-macros.md)