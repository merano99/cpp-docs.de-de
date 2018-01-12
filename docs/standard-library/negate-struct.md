---
title: negate-Struktur | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: xfunctional/std::negate
dev_langs: C++
helpviewer_keywords:
- negate struct
- negate class
ms.assetid: 8a372686-786e-4262-b37c-ca13dc11e62f
caps.latest.revision: "20"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 8d3c8e4999aa3729d0e7961cb976ccc41801e6c6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="negate-struct"></a>negate-Struktur
Ein vordefiniertes Funktionsobjekt, mit dem der arithmetische Negationsvorgang (unäres `operator-`-Element) auf dem Argument ausgeführt wird.  
  
## <a name="syntax"></a>Syntax  
  
```
template <class Type = void>
struct negate : public unary_function<Type, Type>  
{
    Type operator()(const Type& Left) const;
};

// specialized transparent functor for unary operator-
template <>
struct negate<void>  
{
  template <class Type>
  auto operator()(Type&& Left) const`
    -> decltype(-std::forward<Type>(Left));
 };
```  
  
#### <a name="parameters"></a>Parameter  
 `Type`  
 Jeder Typ, der ein `operator-`-Element unterstützt, das einen Operanden des angegebenen oder abgeleiteten Typs akzeptiert.  
  
 `Left`  
 Der zu negierende Operand. Die spezialisierte Vorlage vervollkommnet die Weiterleitung von lvalue und rvalue-Verweisargumenten des abgeleiteten Typs `Type`.  
  
## <a name="return-value"></a>Rückgabewert  
 Das Ergebnis von `-Left.`. Mit der spezialisierten Vorlage wird eine perfekte Weiterleitung des Ergebnisses ausgeführt, das den Typ aufweist, der vom unären `operator-` zurückgegeben wird.  
  
## <a name="example"></a>Beispiel  
  
```cpp  
// functional_negate.cpp  
// compile with: /EHsc  
#include <vector>  
#include <functional>  
#include <algorithm>  
#include <iostream>  
  
using namespace std;  
  
int main( )  
{  
   vector <int> v1, v2 ( 8 );  
   vector <int>::iterator Iter1, Iter2;  
  
   int i;  
   for ( i = -2 ; i <= 5 ; i++ )  
   {  
      v1.push_back( 5 * i );  
   }  
  
   cout << "The vector v1 = ( " ;  
   for ( Iter1 = v1.begin( ) ; Iter1 != v1.end( ) ; Iter1++ )  
      cout << *Iter1 << " ";  
   cout << ")" << endl;  
  
   // Finding the element-wise negatives of the vector v1  
   transform ( v1.begin( ),  v1.end( ), v2.begin( ), negate<int>( ) );  
  
   cout << "The negated elements of the vector = ( " ;  
   for ( Iter2 = v2.begin( ) ; Iter2 != v2.end( ) ; Iter2++ )  
      cout << *Iter2 << " ";  
   cout << ")" << endl;  
}  
\* Output:   
The vector v1 = ( -10 -5 0 5 10 15 20 25 )  
The negated elements of the vector = ( 10 5 0 -5 -10 -15 -20 -25 )  
*\  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<functional>  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [Threadsicherheit in der C++-Standardbibliothek](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [C++-Standardbibliotheksreferenz](../standard-library/cpp-standard-library-reference.md)


