---
title: Compilerfehler C3225
ms.date: 11/04/2016
f1_keywords:
- C3225
helpviewer_keywords:
- C3225
ms.assetid: f5f66973-256e-4298-ac46-c87819cbde34
ms.openlocfilehash: 81316864c9c04c18ca1c96d1e74ad9988734eb72
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50541491"
---
# <a name="compiler-error-c3225"></a>Compilerfehler C3225

generisches Typargument für "Arg" kann nicht 'Typ', es muss ein Werttyp oder ein Handletyp sein

Das generische Typargument hatte nicht den richtigen Typ.

Weitere Informationen finden Sie unter [Generika](../../windows/generics-cpp-component-extensions.md).

## <a name="example"></a>Beispiel

Einen generischen Typ mit der ein systemeigener Typ kann nicht instanziiert werden. Im folgende Beispiel wird die C3225 generiert.

```
// C3225.cpp
// compile with: /clr
class A {};

ref class B {};

generic <class T>
ref class C {};

int main() {
   C<A>^ c = gcnew C<A>;   // C3225
   C<B^>^ c2 = gcnew C<B^>;   // OK
}
```

## <a name="example"></a>Beispiel

Das folgende Beispiel erstellt eine Komponente, die mithilfe von c#. Beachten Sie, dass die Einschränkung gibt an, dass der generische Typ nur mit einem Werttyp instanziiert werden kann.

```
// C3225_b.cs
// compile with: /target:library
// a C# program
public class MyList<T> where T: struct {}
```

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet der c#-Komponente erstellt und verstößt gegen die Einschränkung, die nur MyList sein kann nicht mit einem Werttyp instanziiert <xref:System.Nullable>. Im folgende Beispiel wird die C3225 generiert.

```
// C3225_c.cpp
// compile with: /clr
#using "C3225_b.dll"
ref class A {};
value class B {};
int main() {
   MyList<A> x;   // C3225
   MyList<B> y;   // OK
}
```