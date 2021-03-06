---
title: 'Gleichheitsoperatoren: == und !='
ms.date: 11/04/2016
f1_keywords:
- not_eq
- '!='
- ==
helpviewer_keywords:
- '!= operator'
- equality operator
- not equal to comparison operator
- equality operator [C++], syntax
- == operator
- not_eq operator
- equal to operator
ms.assetid: ba4e9659-2392-4fb4-be5a-910a2a6df45a
ms.openlocfilehash: d6248d4a31c478b62e5fbe304d9bde9b51b7cb06
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50635596"
---
# <a name="equality-operators--and-"></a>Gleichheitsoperatoren: == und !=

## <a name="syntax"></a>Syntax

```
expression == expression
expression != expression
```

## <a name="remarks"></a>Hinweise

Die binären Gleichheitsoperatoren vergleichen die Operanden hinsichtlich strikter Gleichheit oder Ungleichheit.

Die Gleichheitsoperatoren "gleich" (`==`) und "ungleich" (`!=`) haben weniger Vorrang als die relationalen Operatoren, aber sie verhalten sich ähnlich. Der Ergebnistyp für diese Operatoren ist **"bool"**.

Der Ungleichheitsoperator (`==`) gibt **"true"** (1), wenn beide Operanden denselben Wert haben; andernfalls wird **"false"** (0). Der Not-gleich-Operator (`!=`) gibt **"true"** , wenn die Operanden nicht mit den gleichen Wert verfügen, andernfalls **"false"**.

## <a name="operator-keyword-for-"></a>Operator-Schlüsselwort für !=

Der `not_eq`-Operator ist die Textentsprechung von `!=`. Es gibt zwei Möglichkeiten, den Zugriff auf die `not_eq` -Operator in Programmen: Fügen Sie die Headerdatei `iso646.h`, oder Kompilieren Sie mit der [/Za](../build/reference/za-ze-disable-language-extensions.md) -Compileroption (spracherweiterungen deaktivieren).

## <a name="example"></a>Beispiel

```cpp
// expre_Equality_Operators.cpp
// compile with: /EHsc
#include <iostream>

using namespace std;

int main() {
   cout  << boolalpha
         << "The true expression 3 != 2 yields: "
         << (3 != 2) << endl
         << "The false expression 20 == 10 yields: "
         << (20 == 10) << endl;
}
```

Gleichheitsoperatoren können Zeiger auf Member des gleichen Typs vergleichen. In einem solchen Vergleich werden Pointer-to-Member-Konvertierungen ausgeführt. Pointer-to-member können auch mit einem konstanten Ausdruck verglichen werden, der mit 0 ausgewertet wird.

## <a name="see-also"></a>Siehe auch

[Ausdrücke mit binären Operatoren](../cpp/expressions-with-binary-operators.md)<br/>
[C++-Built-in-Operatoren, Rangfolge und Assoziativität](../cpp/cpp-built-in-operators-precedence-and-associativity.md)<br/>
[C-Operatoren (relational) und C-Gleichheitsoperatoren](../c-language/c-relational-and-equality-operators.md)