---
title: 'CDynamicAccessor:: Getcolumnflags | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CDynamicAccessor.GetColumnFlags
- ATL::CDynamicAccessor::GetColumnFlags
- ATL.CDynamicAccessor.GetColumnFlags
- CDynamicAccessor::GetColumnFlags
- GetColumnFlags
dev_langs: C++
helpviewer_keywords: GetColumnFlags method
ms.assetid: b2ba2f3a-2c61-4a49-abfb-75823908ccf4
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: b7d17072f29eb5eb8a114957a5b03e36308e685a
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="cdynamicaccessorgetcolumnflags"></a>CDynamicAccessor::GetColumnFlags
Ruft die Spalteneigenschaften ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      bool GetColumnFlags(   
   DBORDINAL nColumn,   
   DBCOLUMNFLAGS* pFlags    
) const throw( );  
```  
  
#### <a name="parameters"></a>Parameter  
 `nColumn`  
 [in] Die Nummer der Spalte. Die spaltenzählung beginnt mit 1. Der Wert 0 verweist auf die Lesezeichenspalte, sofern vorhanden.  
  
 `pFlags`  
 [out] Ein Zeiger auf eine Bitmaske, die Spaltenmerkmale beschreibt. Siehe "DBCOLUMNFLAGS Enumerated Type" in [IColumnsInfo:: GetColumnInfo](https://msdn.microsoft.com/en-us/library/ms722704.aspx) in der *OLE DB Programmer's Reference*.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt **"true"** , wenn die Spaltenmerkmale erfolgreich abgerufen werden. Andernfalls wird **false**zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Die Nummer der Spalte, die von einem versetzt wird. Die Spalte 0 (null) ist ein Sonderfall; Es ist das Lesezeichen, falls verfügbar.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** atldbcli.h  
  
## <a name="see-also"></a>Siehe auch  
 [CDynamicAccessor-Klasse](../../data/oledb/cdynamicaccessor-class.md)