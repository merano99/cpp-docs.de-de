---
title: Compilerfehler C3205
ms.date: 11/04/2016
f1_keywords:
- C3205
helpviewer_keywords:
- C3205
ms.assetid: 802d306e-5ff3-4491-8a22-c5f1c072d005
ms.openlocfilehash: bd4d17ff2b6a0197db730a53c5846806335c9fd7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50577514"
---
# <a name="compiler-error-c3205"></a>Compilerfehler C3205

Argumentliste für den Vorlagenparameter "Parameter" fehlt.

Ein [Vorlagenparameter](../../cpp/templates-cpp.md) fehlt.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird C3205 generiert:

```cpp
// C3205.cpp
template<template<class> class T> struct A {
   typedef T unparameterized_type;   // C3205
   // try the following line instead
   // typedef T<int> unparameterized_type;
};

template <class T>
struct B {
   typedef int value_type;
};

int main() {
   A<B> x;
}
```