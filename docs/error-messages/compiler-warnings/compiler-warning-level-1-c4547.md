---
title: Compilerwarnung (Stufe 1) C4547
ms.date: 11/04/2016
f1_keywords:
- C4547
helpviewer_keywords:
- C4547
ms.assetid: 3edf1c2e-c0d5-444d-ae83-44a7cce24bb2
ms.openlocfilehash: 3293e07eb7c03c71d582d83e40bc011fa7c1eb11
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50529682"
---
# <a name="compiler-warning-level-1-c4547"></a>Compilerwarnung (Stufe 1) C4547

'Operator': Operator vor dem Komma keine Auswirkungen hat; Operator mit Nebeneffekten erwartet

Der Compiler hat ein falsch formatiertes Kommaausdruck.

Diese Warnung ist standardmäßig deaktiviert. Weitere Informationen finden Sie unter [Compiler Warnings That Are Off by Default](../../preprocessor/compiler-warnings-that-are-off-by-default.md).

Im folgende Beispiel wird die C4547 generiert:

```
// C4547.cpp
// compile with: /W1
#pragma warning (default : 4547)
int i = 0;
int j = 1;
int main() {
   int l = (i != i,0);   // C4547
   // try the following line instead
   // int l = (i != i);
   // or
   // int l = ((void)(i != i),0);
}
```