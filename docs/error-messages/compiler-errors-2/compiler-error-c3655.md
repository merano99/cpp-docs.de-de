---
title: Compilerfehler C3655
ms.date: 11/04/2016
f1_keywords:
- C3655
helpviewer_keywords:
- C3655
ms.assetid: 724919ab-2915-4b61-8794-44648e162d62
ms.openlocfilehash: 268994b2e694c6260a3fc9e9edf102ec0127ee31
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50448602"
---
# <a name="compiler-error-c3655"></a>Compilerfehler C3655

'Funktion': Funktion wurde bereits explizit überschrieben.

Eine Funktion kann nur explizit einmal überschrieben werden. Weitere Informationen finden Sie unter [explizite Überschreibungen](../../windows/explicit-overrides-cpp-component-extensions.md).

Im folgende Beispiel wird die C3655 generiert:

```
// C3655.cpp
// compile with: /clr /c
public ref struct B {
   virtual void f();
   virtual void g();
};

public ref struct D : B {
   virtual void f() new sealed = B::f;
   virtual void g() new sealed = B::f;   // C3655
   // try the following line instead
   // virtual void g() new sealed = B::g;
};
```