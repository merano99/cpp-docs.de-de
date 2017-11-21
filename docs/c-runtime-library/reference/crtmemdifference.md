---
title: _CrtMemDifference | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: _CrtMemDifference
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
- _CrtMemDifference
- CrtMemDifference
dev_langs: C++
helpviewer_keywords:
- CrtMemDifference function
- _CrtMemDifference function
ms.assetid: 0f327278-b551-482f-958b-76941f796ba4
caps.latest.revision: "16"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 32192a01032a710d5b64f90b6680b99393d3caa9
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="crtmemdifference"></a>_CrtMemDifference
Vergleicht zwei Speicherzustände und gibt die vorhandenen Unterschiede zurück (nur Debugversion).  
  
## <a name="syntax"></a>Syntax  
  
```  
int _CrtMemDifference(   
   _CrtMemState *stateDiff,  
   const _CrtMemState *oldState,  
   const _CrtMemState *newState   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `stateDiff`  
 Zeiger auf eine `_CrtMemState` -Struktur, die zum Speichern der Unterschiede zwischen den beiden (zurückgegebenen) Speicherzuständen verwendet wird.  
  
 `oldState`  
 Zeiger auf einen früheren Speicherzustand (`_CrtMemState` -Struktur).  
  
 `newState`  
 Zeiger auf einen späteren Speicherzustand (`_CrtMemState` -Struktur).  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn die Speicherzustände sich erheblich unterscheiden, gibt `_CrtMemDifference` TRUE zurück. Andernfalls gibt die Funktion FALSE zurück.  
  
## <a name="remarks"></a>Hinweise  
 Die `_CrtMemDifference` -Funktion vergleicht `oldState` und `newState` und speichert die vorhandenen Unterschiede in `stateDiff`. Dieser Parameter kann dann von der Anwendung verwendet werden, um Speicherverluste und andere Speicherprobleme zu erkennen. Wenn [_DEBUG](../../c-runtime-library/debug.md) nicht definiert ist, werden Aufrufe von `_CrtMemDifference` während der Vorverarbeitung entfernt.  
  
 `newState` und `oldState` müssen jeweils ein gültiger Zeiger auf eine in „Crtdbg.h“ definierte `_CrtMemState` -Struktur sein, die von [_CrtMemCheckpoint](../../c-runtime-library/reference/crtmemcheckpoint.md) gefüllt wurde, bevor `_CrtMemDifference`aufgerufen wird. `stateDiff` muss ein Zeiger auf eine zuvor zugeordnete Instanz der `_CrtMemState` -Struktur sein. Wenn `stateDiff`, `newState` oder `oldState` `NULL` ist, wird der Handler für ungültige Parameter aufgerufen, wie in [Parametervalidierung](../../c-runtime-library/parameter-validation.md) beschrieben. Wenn die weitere Ausführung zugelassen wird, wird [errno, _doserrno, _sys_errlist und _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md) auf `EINVAL` gesetzt, und die Funktion gibt FALSE zurück.  
  
 `_CrtMemDifference` vergleicht die `_CrtMemState`-Feldwerte der Blöcke in `oldState` mit denen in `newState` und speichert das Ergebnis in `stateDiff`. Wenn sich die Anzahl der zugeordneten Blocktypen oder die Gesamtzahl der zugeordneten Blöcke für jeden Typ in den beiden Speicherzuständen unterscheidet, werden die Zustände als deutlich unterschiedlich bezeichnet. Der Unterschied zwischen der größten Menge, die jemals für beide Zustände gleichzeitig zugeordnet wurde, und der Unterschied zwischen den gesamten Speicherbelegungen für die beiden Zustände werden auch in `stateDiff`gespeichert.  
  
 Standardmäßig sind interne C-Laufzeitblöcke (`_CRT_BLOCK`) nicht in den Speicherzustandsvorgängen enthalten. Die [_CrtSetDbgFlag](../../c-runtime-library/reference/crtsetdbgflag.md) -Funktion kann das `_CRTDBG_CHECK_CRT_DF` -Bit von `_crtDbgFlag` aktiviert werden, um diese Blöcke in die Erkennung von Speicherverlusten und andere Speicherzustandsvorgänge einzuschließen. Freigegebene Speicherblöcke (`_FREE_BLOCK`) führen nicht dazu, dass `_CrtMemDifference` TRUE zurückgibt.  
  
 Weitere Informationen über Heapzustandsfunktionen und die `_CrtMemState` -Struktur finden Sie unter [Heap State Reporting Functions](/visualstudio/debugger/crt-debug-heap-details)aufgerufen wird. Informationen darüber, wie Speicherblöcke in der Debugversion des Basisheaps zugeordnet, initialisiert und verwaltet werden, finden Sie unter [Details zum CRT-Debugheap](/visualstudio/debugger/crt-debug-heap-details).  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|Optionaler Header|  
|-------------|---------------------|---------------------|  
|`_CrtMemDifference`|\<crtdbg.h>|\<errno.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md) in der Einführung.  
  
 **Bibliotheken:** Nur Debugversionen der [CRT-Bibliotheksfunktionen](../../c-runtime-library/crt-library-features.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Debugroutinen](../../c-runtime-library/debug-routines.md)   
 [_crtDbgFlag](../../c-runtime-library/crtdbgflag.md)