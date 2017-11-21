---
title: _aligned_msize | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _aligned_msize
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
- api-ms-win-crt-heap-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _aligned_msize
- aligned_msize
dev_langs:
- C++
helpviewer_keywords:
- aligned_msize function
- _aligned_msize function
ms.assetid: 10995edc-2110-4212-9ca9-5e0220a464f4
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 16d1bf59dfd4b3ef5f037aed9c0f6febfdf1a2e8
ms.openlocfilehash: f4b39fda75013cb69e57b6f8c62bc3155261e1db
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="alignedmsize"></a>_aligned_msize
Gibt die Größe eines im Heap belegten Speicherblocks zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
size_t _msize(  
   void *memblock,  
   size_t alignment,  
   size_t offset  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in] `memblock`  
 Zeiger zum Speicherblock.  
  
 [in] `alignment`  
 Der Ausrichtungswert, der eine ganzzahlige Potenz von 2 sein muss.  
  
 [in] `offset`  
 Der Offset in der Speicherbelegung zum Erzwingen der Ausrichtung.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt die Größe (in Bytes) als ganze Zahl ohne Vorzeichen zurück.  
  
## <a name="remarks"></a>Hinweise  
 Die `_aligned_msize`-Funktion gibt die Größe des Speicherblocks, der durch einen Aufruf von [_aligned_malloc](../../c-runtime-library/reference/aligned-malloc.md) oder [_aligned_realloc](../../c-runtime-library/reference/aligned-realloc.md) belegt wurde, in Byte zurück. Die `alignment`- und `offset`-Werte müssen mit den Werten identisch sein, die an die Funktion übergeben wurden, die den Speicherblock belegt hat.  
  
 Wenn die Anwendung mit einer Debugversion der C-Laufzeitbibliotheken verknüpft ist, wird `_aligned_msize` in [_aligned_msize_dbg](../../c-runtime-library/reference/aligned-msize-dbg.md) aufgelöst. Weitere Informationen dazu, wie der Heap während des Debugprozesses verwaltet wird, finden Sie unter [CRT-Debugheap](/visualstudio/debugger/crt-debug-heap-details).  
  
 Diese Funktion überprüft seine Parameter. Wenn `memblock` ein NULL-Zeiger oder `alignment` keine Potenz von 2 ist, ruft `_msize` einen Handler für ungültige Parameter auf, wie in unter [Parametervalidierung](../../c-runtime-library/parameter-validation.md) beschrieben. Wenn der Fehler behandelt wird, legt die Funktion `errno` auf `EINVAL` fest und gibt -1 zurück.  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|`_msize`|\<malloc.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md) in der Einführung.  
  
## <a name="libraries"></a>Bibliotheken  
 Alle Versionen der [C-Laufzeitbibliotheken](../../c-runtime-library/crt-library-features.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Speicherbelegung](../../c-runtime-library/memory-allocation.md)