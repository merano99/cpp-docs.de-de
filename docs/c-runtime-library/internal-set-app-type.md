---
title: __set_app_type | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- __set_app_type
- _set_app_type
apilocation:
- msvcr90.dll
- msvcr100.dll
- msvcr110.dll
- msvcr80.dll
- msvcrt.dll
- msvcr120.dll
- msvcr110_clr0400.dll
- api-ms-win-crt-runtime-l1-1-0.dll
apitype: DLLExport
f1_keywords: __set_app_type
dev_langs: C++
helpviewer_keywords: __set_app_type
ms.assetid: f0ac0f4d-70e6-4e96-9e43-eb9d1515490c
caps.latest.revision: "2"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 4eb5a061e2468c9590dd49c7ae2306091b397aa3
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="setapptype"></a>__set_app_type
Legt den aktuellen Anwendungstyp fest.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
void __set_app_type (  
   int at  
   )  
```  
  
#### <a name="parameters"></a>Parameter  
 `at`  
 Ein Wert, der den Anwendungstyp angibt. Mögliche Werte sind:  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|_UNKNOWN_APP|Unbekannter Anwendungstyp.|  
|_CONSOLE_APP|Konsolenanwendung (für Befehlszeilen).|  
|_GUI_APP|GUI-Anwendung (in Windows).|  
  
## <a name="remarks"></a>Hinweise  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|__set_app_type|internal.h|