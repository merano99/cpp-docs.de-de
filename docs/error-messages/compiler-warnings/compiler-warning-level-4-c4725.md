---
title: Compilerwarnung (Stufe 4) C4725
ms.date: 11/04/2016
f1_keywords:
- C4725
helpviewer_keywords:
- C4725
ms.assetid: effa0335-71c3-4b3b-8618-da4b9b46a95d
ms.openlocfilehash: 9da830133bbca2abcd5fa77339e698b35dae32f6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50455639"
---
# <a name="compiler-warning-level-4-c4725"></a>Compilerwarnung (Stufe 4) C4725

Anweisung kann auf einigen Pentium-Prozessoren ungenau sein

Der Code enthält eine Inlineassemblyanweisung, die auf einigen Pentium-Mikroprozessoren möglicherweise keine genauen Ergebnisse erzeugen kann.

Im folgenden Beispiel wird C4725 generiert:

```
// C4725.cpp
// compile with: /W4
// processor: x86
double m32fp = 2.0003e-17;

void f() {
   __asm
   {
      FDIV m32fp   // C4725
   }
}

int main() {
}
```