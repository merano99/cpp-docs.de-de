---
title: _com_error::ErrorMessage | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: _com_error::ErrorMessage
dev_langs: C++
helpviewer_keywords: ErrorMessage method [C++]
ms.assetid: e47335b6-01af-4975-a841-121597479eb7
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 0b60c0f74cd350382b6cf8669361087dee601fe4
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="comerrorerrormessage"></a>_com_error::ErrorMessage
**Microsoft-spezifisch**  
  
 Ruft die Zeichenfolgenmeldung für das `HRESULT`-Objekt ab, das im `_com_error`-Objekt gespeichert ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
const TCHAR * ErrorMessage( ) const throw( );  
  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt die Zeichenfolgenmeldung für das `HRESULT`-Objekt zurück, das innerhalb des `_com_error`-Objekts aufgezeichnet wird. Wenn die `HRESULT` ist ein zugeordneter 16-Bit [wCode](../cpp/com-error-wcode.md), wird eine generische Meldung "`IDispatch error #<wCode>`" wird zurückgegeben. Wenn keine Nachricht gefunden wird, wird eine generische Meldung "`Unknown error #<hresult>`" zurückgegeben. Die zurückgegebene Zeichenfolge ist entweder eine Unicode- oder multibyte-Zeichenfolge, abhängig vom Status des der **_UNICODE** Makro.  
  
## <a name="remarks"></a>Hinweise  
 Ruft den entsprechenden Systemnachrichtentext für das `HRESULT`-Objekt ab, das innerhalb des `_com_error`-Objekts erfasst ist. Der systemnachrichtentext wird durch Aufruf der Win32 abgerufen [FormatMessage](http://msdn.microsoft.com/library/windows/desktop/ms679351) Funktion. Die zurückgegebene Zeichenfolge wird von der `FormatMessage`-API zugeordnet und wird ausgegeben, wenn das `_com_error`-Objekt zerstört wird.  
  
 **Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [_com_error-Klasse](../cpp/com-error-class.md)