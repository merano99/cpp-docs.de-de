---
title: __vmx_off
ms.date: 11/04/2016
f1_keywords:
- __vmx_off
helpviewer_keywords:
- VMXOFF instruction
- __vmx_off intrinsic
ms.assetid: 78a32d46-9291-406c-b982-a550855aff18
ms.openlocfilehash: 24f57195b60a788c0189a295fa7b6e4818a93d83
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50440286"
---
# <a name="vmxoff"></a>__vmx_off

**Microsoft-spezifisch**

VM-Erweiterungen (VMX) Vorgang im Prozessor wird deaktiviert.

## <a name="syntax"></a>Syntax

```
void __vmx_off();
```

## <a name="remarks"></a>Hinweise

Die `__vmx_off` -Funktion entspricht der `VMXOFF` -Computeranweisung. Diese Funktion unterstützt die Interaktion zwischen dem Monitor des virtuellen Computers eines Hosts mit einem Gastbetriebssystem und seinen Anwendungen. Dokumentieren Sie weitere Informationen suchen Sie nach dem Dokument "Intel Virtualization Technical Specification for the IA-32 Intel Architecture," Dokumentnummer C97063-002 auf der [Intel Corporation](https://software.intel.com/articles/intel-sdm) Standort.

## <a name="requirements"></a>Anforderungen

|Systemintern|Architektur|
|---------------|------------------|
|`__vmx_off`|x86, x64|

**Headerdatei** \<intrin.h >

**Ende Microsoft-spezifisch**

## <a name="see-also"></a>Siehe auch

[Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)