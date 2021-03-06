---
title: 'Gewusst wie: Abfangen von Ausnahmen, die von der MSIL ausgelöst wurden, in nativem Code'
ms.date: 11/04/2016
helpviewer_keywords:
- exceptions, catching
- catching exceptions, thrown from MSIL
- MSIL, catching exceptions in native code
ms.assetid: c15afd2b-8505-43bf-8a4a-f1d41532a124
ms.openlocfilehash: 73c9a9af66a6e292c76b96ec47a5853684e602f9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50635611"
---
# <a name="how-to-catch-exceptions-in-native-code-thrown-from-msil"></a>Gewusst wie: Abfangen von Ausnahmen, die von der MSIL ausgelöst wurden, in nativem Code

In nativem Code können Sie native C++-Ausnahme von der MSIL abfangen.  Sie können auch mit CLR-Ausnahmen abfangen `__try` und `__except`.

Weitere Informationen finden Sie unter [Structured Exception Handling (C/C++)](../cpp/structured-exception-handling-c-cpp.md) und [C++-Ausnahmebehandlung](../cpp/cpp-exception-handling.md).

## <a name="example"></a>Beispiel

Im folgende Beispiel definiert ein Modul mit zwei Funktionen, eine, die von einem systemeigenen Ausnahme ausgelöst und eine, die eine MSIL-Ausnahme auslöst.

```
// catch_MSIL_in_native.cpp
// compile with: /clr /c
void Test() {
   throw ("error");
}

void Test2() {
   throw (gcnew System::Exception("error2"));
}
```

## <a name="example"></a>Beispiel

Im folgende Beispiel definiert ein Modul, das einen einheitlichen und MSIL-Ausnahme abfängt.

```
// catch_MSIL_in_native_2.cpp
// compile with: /clr catch_MSIL_in_native.obj
#include <iostream>
using namespace std;
void Test();
void Test2();

void Func() {
   // catch any exception from MSIL
   // should not catch Visual C++ exceptions like this
   // runtime may not destroy the object thrown
   __try {
      Test2();
   }
   __except(1) {
      cout << "caught an exception" << endl;
   }

}

int main() {
   // catch native C++ exception from MSIL
   try {
      Test();
   }
   catch(char * S) {
      cout << S << endl;
   }
   Func();
}
```

```Output
error
caught an exception
```

## <a name="see-also"></a>Siehe auch

[Ausnahmebehandlung](../windows/exception-handling-cpp-component-extensions.md)