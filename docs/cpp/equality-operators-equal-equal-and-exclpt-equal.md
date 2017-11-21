---
title: 'Gleichheitsoperatoren: == und! = | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- not_eq
- '!='
- ==
dev_langs: C++
helpviewer_keywords:
- '!= operator'
- equality operator
- not equal to comparison operator
- equality operator [C++], syntax
- == operator
- not_eq operator
- equal to operator
ms.assetid: ba4e9659-2392-4fb4-be5a-910a2a6df45a
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: a064ca4c4d490d89705ffa30deb4eb132002cd16
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="equality-operators--and-"></a>Gleichheitsoperatoren: == und !=
## <a name="syntax"></a>Syntax  
  
```  
expression == expression  
expression != expression  
```  
  
## <a name="remarks"></a>Hinweise  
 Die binären Gleichheitsoperatoren vergleichen die Operanden hinsichtlich strikter Gleichheit oder Ungleichheit.  
  
 Die Gleichheitsoperatoren "gleich" (`==`) und "ungleich" (`!=`) haben weniger Vorrang als die relationalen Operatoren, aber sie verhalten sich ähnlich. Der Ergebnistyp für diese Operatoren ist `bool`.  
  
 Der Ungleichheitsoperator (`==`) gibt **"true"** (1), wenn beide Operanden den gleichen Wert haben; andernfalls wird zurückgegeben **"false"** (0). Der Not-gleich-Operator (`!=`) gibt **"true"** , wenn die Operanden nicht denselben Wert haben, andernfalls wird zurückgegeben **"false"**.  
  
## <a name="operator-keyword-for-"></a>Operator-Schlüsselwort für !=  
 Der `not_eq`-Operator ist die Textentsprechung von `!=`. Es gibt zwei Möglichkeiten, den Zugriff auf die `not_eq` -Operator in Programmen: Fügen Sie die Headerdatei `iso646.h`, oder Kompilieren Sie mit der ["/ Za"](../build/reference/za-ze-disable-language-extensions.md) -Compileroption (spracherweiterungen deaktivieren).  
  
## <a name="example"></a>Beispiel  
  
```  
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
 [Ausdrücke mit binären Operatoren](../cpp/expressions-with-binary-operators.md)   
 [Integrierte C++-Operatoren, Rangfolge und Assoziativität](../cpp/cpp-built-in-operators-precedence-and-associativity.md)   
 [C-Operatoren (relational) und C-Gleichheitsoperatoren](../c-language/c-relational-and-equality-operators.md)