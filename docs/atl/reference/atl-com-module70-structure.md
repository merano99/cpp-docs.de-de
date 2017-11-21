---
title: _ATL_COM_MODULE70 Struktur | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::_ATL_COM_MODULE70
- ATL._ATL_COM_MODULE70
- _ATL_COM_MODULE70
dev_langs: C++
helpviewer_keywords:
- _ATL_COM_MODULE70 structure
- ATL_COM_MODULE70 structure
ms.assetid: 5b0b2fd0-bdeb-4c7e-8870-78fa69ace6e6
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: a269820c5a0965553989bc57d7c239aa95e527ef
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="atlcommodule70-structure"></a>_ATL_COM_MODULE70-Struktur
Verwendung durch COM-bezogenen Code in ATL  
  
## <a name="syntax"></a>Syntax  
  
```
struct _ATL_COM_MODULE70 {
    UINT cbSize;
    HINSTANCE m_hInstTypeLib;
    _ATL_OBJMAP_ENTRY** m_ppAutoObjMapFirst;
    _ATL_OBJMAP_ENTRY** m_ppAutoObjMapLast;
    CRITICAL_SECTION m_csObjMap;
};
```  
  
## <a name="members"></a>Member  
 `cbSize`  
 Die Größe der Struktur, die für die versionsverwaltung verwendet.  
  
 `m_hInstTypeLib`  
 Die Handle-Instanz, auf die Typbibliothek für dieses Modul.  
  
 **m_ppAutoObjMapFirst**  
 Die Adresse des Arrayelements, der angibt, der des Anfang der Objekt-Zuordnungseinträge für dieses Modul.  
  
 **m_ppAutoObjMapLast**  
 Die Adresse des Arrayelements, die das Ende der Objekt-Zuordnungseinträge für dieses Modul.  
  
 `m_csObjMap`  
 Kritischen Abschnitt, um die Serialisierung des Zugriffs auf die Objekt-Zuordnungseinträge. Wird intern vom ATL verwendet  
  
## <a name="remarks"></a>Hinweise  
 [_ATL_COM_MODULE](atl-typedefs.md#_atl_com_module) ist definiert als Typedef von `_ATL_COM_MODULE70`.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** atlbase.h  
  
## <a name="see-also"></a>Siehe auch  
 [Strukturen](../../atl/reference/atl-structures.md)




