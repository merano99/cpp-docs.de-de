---
title: CComClassFactoryAutoThread Klasse | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CComClassFactoryAutoThread
- ATLCOM/ATL::CComClassFactoryAutoThread
- ATLCOM/ATL::CComClassFactoryAutoThread::CreateInstance
- ATLCOM/ATL::CComClassFactoryAutoThread::LockServer
dev_langs: C++
helpviewer_keywords: CComClassFactoryAutoThread class
ms.assetid: 22008042-533f-4dd9-bf7e-191ee571f9a1
caps.latest.revision: "21"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: dfeadfba46f1dd0b033f3d82571e82c59a449ec9
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="ccomclassfactoryautothread-class"></a>CComClassFactoryAutoThread-Klasse
Diese Klasse implementiert die [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364) Schnittstelle, und ermöglicht es Objekten, die in mehreren Apartments erstellt werden.  
  
> [!IMPORTANT]
>  Diese Klasse und ihre Member können nicht in Anwendungen verwendet werden, die in der Windows-Runtime ausgeführt.  
  
## <a name="syntax"></a>Syntax  
  
```
class CComClassFactoryAutoThread 
   : public IClassFactory, 
     public CComObjectRootEx<CComGlobalsThreadModel>
```  
  
## <a name="members"></a>Mitglieder  
  
### <a name="public-methods"></a>Öffentliche Methoden  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CComClassFactoryAutoThread::CreateInstance](#createinstance)|Erstellt ein Objekt der angegebenen CLSID.|  
|[CComClassFactoryAutoThread::LockServer](#lockserver)|Sperrt die Klassenfactory im Arbeitsspeicher.|  
  
## <a name="remarks"></a>Hinweise  
 `CComClassFactoryAutoThread`ähnelt dem [CComClassFactory](../../atl/reference/ccomclassfactory-class.md), aber ermöglicht es Objekten, die in mehreren Apartments erstellt werden. Dieser Unterstützung profitieren zu können, leiten Sie die EXE-Moduls aus [CComAutoThreadModule](../../atl/reference/ccomautothreadmodule-class.md).  
  
 ATL-Objekte abrufen eine Klassenfactory normalerweise durch Ableiten von [CComCoClass](../../atl/reference/ccomcoclass-class.md). Diese Klasse enthält das Makro [DECLARE_CLASSFACTORY](aggregation-and-class-factory-macros.md#declare_classfactory), die deklariert wird, [CComClassFactory](../../atl/reference/ccomclassfactory-class.md) als der standardfactory-Klasse. Mit `CComClassFactoryAutoThread`, geben Sie die [DECLARE_CLASSFACTORY_AUTO_THREAD](aggregation-and-class-factory-macros.md#declare_classfactory_auto_thread) Makro in die Definition der Klasse des Objekts. Zum Beispiel:  
  
 [!code-cpp[NVC_ATL_COM#9](../../atl/codesnippet/cpp/ccomclassfactoryautothread-class_1.h)]  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 `CComObjectRootBase`  
  
 [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)  
  
 `IClassFactory`  
  
 `CComClassFactoryAutoThread`  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** atlcom.h  
  
##  <a name="createinstance"></a>CComClassFactoryAutoThread::CreateInstance  
 Erstellt ein Objekt der angegebenen CLSID und ruft einen Schnittstellenzeiger für dieses Objekt ab.  
  
```
STDMETHODIMP CreateInstance(
    LPUNKNOWN pUnkOuter,
    REFIID riid,
    void** ppvObj);
```  
  
### <a name="parameters"></a>Parameter  
 `pUnkOuter`  
 [in] Wenn das Objekt als Teil einer Aggregatfunktion gehört, dann erstellt wird `pUnkOuter` muss die äußere unbekannte sein. Andernfalls `pUnkOuter` muss **NULL**.  
  
 `riid`  
 [in] Die IID der angeforderten Schnittstelle. Wenn `pUnkOuter` nicht **NULL**, `riid` muss **IID_IUnknown**.  
  
 `ppvObj`  
 [out] Ein Zeiger auf den Schnittstellenzeiger, der durch `riid`. Wenn das Objekt nicht über diese Schnittstelle unterstützt `ppvObj` festgelegt ist, um **NULL**.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Standard `HRESULT` -Wert.  
  
### <a name="remarks"></a>Hinweise  
 Wenn Ihr Modul abgeleitet [CComAutoThreadModule](../../atl/reference/ccomautothreadmodule-class.md), `CreateInstance` zuerst wählt einen Thread zum Erstellen des Objekts im zugeordneten Apartment.  
  
##  <a name="lockserver"></a>CComClassFactoryAutoThread::LockServer  
 Erhöht und verringert die Sperrenanzahl Modul durch Aufrufen von **_Module::Lock** und **_Module::Unlock**zugeordnet.  
  
```
STDMETHODIMP LockServer(BOOL fLock);
```  
  
### <a name="parameters"></a>Parameter  
 `fLock`  
 [in] Wenn **"true"**die Anzahl der Sperren andernfalls erhöht, wird die Anzahl der Sperren wird verringert.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Standard `HRESULT` -Wert.  
  
### <a name="remarks"></a>Hinweise  
 Bei Verwendung `CComClassFactoryAutoThread`, **_Module** bezieht sich normalerweise auf die globale Instanz von [CComAutoThreadModule](../../atl/reference/ccomautothreadmodule-class.md).  
  
 Aufrufen von `LockServer` ermöglicht einem Client zu einer Klassenfactory festzuhalten, sodass mehrere Objekte schnell erstellt werden können.  
  
## <a name="see-also"></a>Siehe auch  
 [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364)   
 [CComClassFactory2-Klasse](../../atl/reference/ccomclassfactory2-class.md)   
 [CComClassFactorySingleton-Klasse](../../atl/reference/ccomclassfactorysingleton-class.md)   
 [CComObjectRootEx-Klasse](../../atl/reference/ccomobjectrootex-class.md)   
 [CComGlobalsThreadModel](atl-typedefs.md#ccomglobalsthreadmodel)   
 [Klassenübersicht](../../atl/atl-class-overview.md)