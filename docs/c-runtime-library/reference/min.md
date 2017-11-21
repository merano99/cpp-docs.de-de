---
title: __min | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: __min
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- __min
- min
- _min
dev_langs: C++
helpviewer_keywords:
- __min macro
- min macro
- minimum macro
- _min macro
ms.assetid: 2037f26c-b48a-4a69-8870-22519f052a3c
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: a80f679834971f8508f5f586758dced1e5f6ed9d
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="min"></a>__min
Gibt den kleineren der beiden Werte zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
type __min(  
   type a,  
   type b   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `type`  
 Jeder beliebige numerische Datentyp.  
  
 `a, b`  
 Werte von einem numerischen Datentyp, der verglichen werden soll.  
  
## <a name="return-value"></a>Rückgabewert  
 Das kleinere der beiden Argumente.  
  
## <a name="remarks"></a>Hinweise  
 Das `__min`-Makro vergleicht zwei Werte und gibt den kleineren Wert zurück. Die Argumente können von einen beliebigen Datentyp stammen, signed oder unsigned. Beide Argumente sowie der Rückgabewert müssen demselben Datentyp entsprechen.  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|`__min`|\<stdlib.h>|  
  
## <a name="example"></a>Beispiel  
  
```  
// crt_minmax.c  
  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
   int a = 10;  
   int b = 21;  
  
   printf( "The larger of %d and %d is %d\n",  a, b, __max( a, b ) );  
   printf( "The smaller of %d and %d is %d\n", a, b, __min( a, b ) );  
}  
```  
  
```Output  
The larger of 10 and 21 is 21  
The smaller of 10 and 21 is 10  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Gleitkommaunterstützung](../../c-runtime-library/floating-point-support.md)   
 [__max](../../c-runtime-library/reference/max.md)