---
title: _com_ptr_t::GetActiveObject | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- _com_ptr_t::GetActiveObject
dev_langs:
- C++
helpviewer_keywords:
- GetActiveObject method [C++]
ms.assetid: 2fa94853-0410-4620-91f2-136dae923f9f
caps.latest.revision: 9
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: a61e41c750fdf5865a475d92ba9e1def0aefd748
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="comptrtgetactiveobject"></a>_com_ptr_t::GetActiveObject
**Microsoft-spezifisch**  
  
 Fügt einer vorhandenen Instanz eines Objekts mit einem **CLSID** oder **ProgID**.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      HRESULT GetActiveObject(  
   const CLSID& rclsid   
) throw( );  
HRESULT GetActiveObject(  
   LPCWSTR clsidString   
) throw( );  
HRESULT GetActiveObject(  
   LPCSTR clsidStringA   
) throw( );  
```  
  
#### <a name="parameters"></a>Parameter  
 `rclsid`  
 Die **CLSID** eines Objekts.  
  
 `clsidString`  
 Eine Unicodezeichenfolge, die entweder eine **CLSID** (beginnend mit "**{**") oder ein **ProgID**.  
  
 `clsidStringA`  
 Eine mehrbytezeichenfolge mit der ANSI-Codepage, die entweder eine **CLSID** (beginnend mit "**{**") oder ein **ProgID**.  
  
## <a name="remarks"></a>Hinweise  
 Diese Memberfunktionen rufen `GetActiveObject` auf, um einen Zeiger auf ein ausgeführtes Objekt abzurufen, das mit OLE registriert wurde und dann den Schnittstellentyp des intelligenten Zeigers abfragt. Das Zeigerergebnis wird dann innerhalb dieses `_com_ptr_t`-Objekts gekapselt. **Version** wird aufgerufen, um den Verweiszähler für den zuvor gekapselten Zeiger zu verringern. Diese Routine gibt `HRESULT` zurück, um einen Erfolg oder Fehler anzuzeigen.  
  
-   **GetActiveObject (**`rclsid`**)** Fügt einer vorhandenen Instanz eines Objekts mit einem **CLSID**.      
  
-   **GetActiveObject (**`clsidString`**)** Fügt einer vorhandenen Instanz eines Objekts mit der eine Unicodezeichenfolge, die entweder eine **CLSID** (beginnend mit "**{**") oder ein **ProgID**.      
  
-   **GetActiveObject (**`clsidStringA`**)** Fügt einer vorhandenen Instanz eines Objekts mit einer Multibyte-Zeichenfolge, die entweder eine **CLSID** (beginnend mit "**{**") oder ein **ProgID**.     Aufrufe [MultiByteToWideChar](http://msdn.microsoft.com/library/windows/desktop/dd319072), die davon ausgeht, dass die Zeichenfolge in die ANSI-Codepage anstatt eine OEM-Codepage.  
  
 **Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [_com_ptr_t-Klasse](../cpp/com-ptr-t-class.md)