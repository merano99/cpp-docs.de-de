---
title: __outwordstring
ms.date: 11/04/2016
f1_keywords:
- __outwordstring
helpviewer_keywords:
- rep outsw instruction
- __outwordstring intrinsic
- outsw instruction
ms.assetid: b470c7a0-1de9-4370-886a-b2c3a1f842f4
ms.openlocfilehash: df7ca6ddbb80c21397beb91b8e671f248f2a1d9c
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326289"
---
# <a name="outwordstring"></a>__outwordstring

**Microsoft-spezifisch**

Generiert die `rep outsw` -Anweisung, die sendet `Count` Wörter, die beginnend bei `Buffer` der e/a-Port anhand des `Port`.

## <a name="syntax"></a>Syntax

```
void __outwordstring(
   unsigned short Port,
   unsigned short* Buffer,
   unsigned long Count
);
```

#### <a name="parameters"></a>Parameter

*Port*<br/>
[in] Der Port, der die Daten zu senden.

*Buffer*<br/>
[in] Ein Zeiger auf Daten, die über den angegebenen Port gesendet werden.

*Anzahl*<br/>
[in] Die Anzahl von Wörtern zu senden.

## <a name="requirements"></a>Anforderungen

|Systemintern|Architektur|
|---------------|------------------|
|`__outwordstring`|x86, x64|

**Headerdatei** \<intrin.h >

## <a name="remarks"></a>Hinweise

Diese Routine ist nur als systeminterne Funktion verfügbar.

**Ende Microsoft-spezifisch**

## <a name="see-also"></a>Siehe auch

[Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)