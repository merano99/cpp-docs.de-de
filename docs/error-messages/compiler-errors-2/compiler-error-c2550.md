---
title: Compilerfehler C2550
ms.date: 11/04/2016
f1_keywords:
- C2550
helpviewer_keywords:
- C2550
ms.assetid: 3293f53e-ee66-4035-920d-34e115c3a24c
ms.openlocfilehash: 2df6ae70be31bc519e6cfd826646073becf1ad61
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50462672"
---
# <a name="compiler-error-c2550"></a>Compilerfehler C2550

"Bezeichner": Initialisierungslisten für Konstruktoren dürfen nur in Konstruktordefinition stehen

Eine Initialisiererliste Basisklasse wird auf die Definition einer Funktion verwendet, die kein Konstruktor ist.

Im folgende Beispiel wird die C2550 generiert:

```
// C2550.cpp
// compile with: /c
class C {
public:
   C();
};

class D : public C {
public:
   D();
   void func();
};

void D::func() : C() {}  // C2550
D::D() : C() {}   // OK
```