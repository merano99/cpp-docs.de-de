---
title: CInvalidArgException Klasse | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CInvalidArgException
- AFX/CInvalidArgException
- AFX/CInvalidArgException::CInvalidArgException
dev_langs: C++
helpviewer_keywords: CInvalidArgException [MFC], CInvalidArgException
ms.assetid: e43d7c67-1157-47f8-817a-804083e8186e
caps.latest.revision: "19"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 832f7eed61ce7e11f4840d4d39f51bb807a0011b
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="cinvalidargexception-class"></a>CInvalidArgException-Klasse
Diese Klasse stellt eine Ausnahmebedingung für ein ungültiges Argument dar.  
  
## <a name="syntax"></a>Syntax  
  
```  
class CInvalidArgException : public CSimpleException  
```  
  
## <a name="members"></a>Mitglieder  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CInvalidArgException::CInvalidArgException](#cinvalidargexception)|Der Konstruktor.|  
  
## <a name="remarks"></a>Hinweise  
 Ein `CInvalidArgException` -Objekt stellt eine Ausnahmebedingung für ein ungültiges Argument dar.  
  
 Weitere Informationen zu Exception Handling, finden Sie unter der [CException-Klasse](../../mfc/reference/cexception-class.md) Thema und [Ausnahmebehandlung (MFC)](../../mfc/exception-handling-in-mfc.md).  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CException](../../mfc/reference/cexception-class.md)  
  
 [CSimpleException](../../mfc/reference/csimpleexception-class.md)  
  
 `CInvalidArgException`  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** afx.h  
  
##  <a name="cinvalidargexception"></a>CInvalidArgException::CInvalidArgException  
 Der Konstruktor.  
  
```  
CInvalidArgException();
```  
  
### <a name="remarks"></a>Hinweise  
 Verwenden Sie diesen Konstruktor nicht direkt auf; Rufen Sie die globale Funktion **AfxThrowInvalidArgException**.  
  
## <a name="see-also"></a>Siehe auch  
 [Hierarchiediagramm](../../mfc/hierarchy-chart.md)   
 [CSimpleException-Klasse](../../mfc/reference/csimpleexception-class.md)