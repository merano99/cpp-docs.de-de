---
title: Compilerfehler C2586
ms.date: 11/04/2016
f1_keywords:
- C2586
helpviewer_keywords:
- C2586
ms.assetid: dae703c7-5c38-4db6-8411-4d1b22713eb5
ms.openlocfilehash: a6af49bba84eded7d530f6ecc37fac8f6acf16e2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50519846"
---
# <a name="compiler-error-c2586"></a>Compilerfehler C2586

fehlerhafte benutzerdefinierte Konvertierungssyntax: Unzulässige Dereferenzierungen

Dereferenzierung eines Konvertierungsoperators ist nicht zulässig.

Im folgende Beispiel wird die C2586 generiert:

```
// c2586.cpp
// compile with: /c
struct C {
   * operator int();   // C2586
   operator char();   // OK
};
```