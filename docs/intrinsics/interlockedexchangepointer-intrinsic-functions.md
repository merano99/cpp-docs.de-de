---
title: Systeminterne Funktionen "_InterlockedExchangePointer" | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- _InterlockedExchangePointer_cpp
- _InterlockedExchangePointer_rel
- _InterlockedExchangePointer_nf
- _InterlockedExchangePointer_HLERelease
- _InterlockedExchangePointer_acq
- _InterlockedExchangePointer
- _InterlockedExchangePointer_acq_cpp
- _InterlockedExchangePointer_HLEAcquire
dev_langs: C++
helpviewer_keywords:
- _InterlockedExchangePointer_rel intrinsic
- _InterlockedExchangePointer_HLERelease intrinsic
- _InterlockedExchangePointer intrinsic
- _InterlockedExchangePointer_nf intrinsic
- _InterlockedExchangePointer_acq intrinsic
- _InterlockedExchangePointer_HLEAcquire intrinsic
- InterlockedExchangePointer_acq intrinsic
- InterlockedExchangePointer intrinsic
ms.assetid: 0eaca0b0-d79e-406b-892d-b3b462c50bbb
caps.latest.revision: "17"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: d4c55ce7c11305344156677fbcfce7ef7dd7b117
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="interlockedexchangepointer-intrinsic-functions"></a>Intrinsische Funktionen „_InterlockedExchangePointer“
**Microsoft-spezifisch**  
  
 Führen Sie einen unteilbaren Austauschvorgang durch, bei dem die übergebene Adresse als zweites Argument in das erste kopiert und die ursprüngliche Adresse des ersten Arguments zurückgegeben wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
void * _InterlockedExchangePointer(  
   void * volatile * Target,  
   void * Value  
);   
void * _InterlockedExchangePointer_acq(  
   void * volatile * Target,  
   void * Value  
);   
void * _InterlockedExchangePointer_rel(  
   void * volatile * Target,  
   void * Value  
);   
void * _InterlockedExchangePointer_nf(  
   void * volatile * Target,  
   void * Value  
);   
void * _InterlockedExchangePointer_HLEAcquire(  
   void * volatile * Target,  
   void * Value  
);   
void * _InterlockedExchangePointer_HLERelease(  
   void * volatile * Target,  
   void * Value  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in, out] `Target`  
 Zeiger auf den Zeiger auf den auszutauschenden Wert. Die Funktion setzt den Wert auf `Value` und gibt den vorherigen Wert zurück.  
  
 [in] `Value`  
 Wert, der mit dem Wert ausgetauscht werden soll, auf den von `Target` gezeigt wird.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Funktion gibt den Anfangswert zurück, auf den `Target` zeigt.  
  
## <a name="requirements"></a>Anforderungen  
  
|Systemintern|Architektur|Header|  
|---------------|------------------|------------|  
|`_InterlockedExchangePointer`|x86, ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<INTRIN.h >|  
|`_InterlockedExchangePointer_acq`, `_InterlockedExchangePointer_rel`, `_InterlockedExchangePointer_nf`|ARM|\<INTRIN.h >|  
|`_InterlockedExchangePointer_HLEAcquire`, `_InterlockedExchangePointer_HLERelease`|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)] mit HLE-Unterstützung|\<"immintrin.h" >|  
  
 In der x86-Architektur ist `_InterlockedExchangePointer` ein Makro, das `_InterlockedExchange` aufruft.  
  
## <a name="remarks"></a>Hinweise  
 In einem 64-Bit-System sind die Parameter 64 Bits und müssen auf 64-Bit-Grenzen ausgerichtet sein. Andernfalls schlägt die Funktion fehl. In einem 32-Bit-System sind die Parameter 32 Bits und müssen auf 32-Bit-Grenzen ausgerichtet sein. Weitere Informationen finden Sie unter [ausrichten](../cpp/align-cpp.md).  
  
 Verwenden Sie auf ARM-Plattformen die systeminternen Funktionen mit den Suffixen `_acq` und `_rel`, wenn Sie Semantiken abrufen und freigeben müssen, beispielsweise am Anfang und Ende eines kritischen Abschnitts. Die systeminternen Funktionen mit dem Suffix `_nf` („keine Umgrenzung“) fungieren nicht als Arbeitsspeicherbarriere.  
  
 Auf Intel-Plattformen, die Hardware Lock Elision (HLE)-Anweisungen unterstützen, enthalten die systeminternen Funktionen mit den Suffixen `_HLEAcquire` und `_HLERelease` einen Hinweis für den Prozessor, wie die Leistung durch den Wegfall der Schreibsperre in der Hardware beschleunigt werden kann. Wenn diese systeminternen Funktionen auf Plattformen aufgerufen werden, die HLE nicht unterstützen, wird der Hinweis ignoriert.  
  
 Diese Routinen sind nur als systeminterne Funktionen verfügbar.  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)   
 [Konflikt mit dem x86-Compiler](../build/conflicts-with-the-x86-compiler.md)