---
title: Compilerfehler C3210
ms.date: 11/04/2016
f1_keywords:
- C3210
helpviewer_keywords:
- C3210
ms.assetid: c6e9d309-fabc-4e7d-b526-be20d9fe3f6a
ms.openlocfilehash: 9e0ac1aded7eef40be0e923b3ac1ebc9ef00c7a6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50528738"
---
# <a name="compiler-error-c3210"></a>Compilerfehler C3210

'Typ': Zugriffsdeklaration kann nur auf ein Basisklassenmember angewendet werden

Ein [using-Deklaration](../../cpp/using-declaration.md) wurde falsch angegeben.

## <a name="example"></a>Beispiel

Im folgende Beispiel wird die C3210 generiert.

```
// C3210.cpp
// compile with: /c
struct A {
protected:
   int i;
};

struct B {
   using A::i;   // C3210
};

struct C : public A {
   using A::i;   // OK
};
```