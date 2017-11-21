---
title: Map::Operator(STL/CLR) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::map::operator[]
dev_langs: C++
helpviewer_keywords: operatormember [] [STL/CLR]
ms.assetid: 50e494c5-62d4-4469-8da3-7432ee4dff97
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 9851c754186ebc5e30cd0757cf9f1723625bdd92
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="mapoperatorstlclr"></a>map::operator(STL/CLR)
Ein Schlüssel auf den zugehörigen zugeordneten Wert zugeordnet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
mapped_type operator[](key_type key);  
```  
  
#### <a name="parameters"></a>Parameter  
 Key  
 Der zu suchende Schlüsselwert.  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktionen, die Aufgaben nach einem Element mit der entsprechenden Reihenfolge zu suchen `key`. Wenn ein solches gefunden wird, wird der zugeordnete zugeordneten Wert zurückgegeben; andernfalls fügt `value_type(key, mapped_type())` und gibt das zugeordnete (Standard) zugeordneten Wert. Sie verwenden es, um einen zugeordneten Wert erhält seinen zugehörige Schlüssel suchen oder um sicherzustellen, dass ein Eintrag für den Schlüssel vorhanden ist, wenn keiner gefunden wird.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_map_operator_sub.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
int main()   
    {   
    Mymap c1;   
    c1.insert(Mymap::make_value(L'a', 1));   
    c1.insert(Mymap::make_value(L'b', 2));   
    c1.insert(Mymap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("c1[{0}] = {1}",   
        L'A', c1[L'A']);   
    System::Console::WriteLine("c1[{0}] = {1}",   
        L'b', c1[L'b']);   
  
// redisplay altered contents   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// alter mapped values and redisplay   
    c1[L'A'] = 10;   
    c1[L'c'] = 13;   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
 [a 1] [b 2] [c 3]  
c1[A] = 0  
c1[b] = 2  
 [A 0] [a 1] [b 2] [c 3]  
 [A 10] [a 1] [b 2] [c 13]  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Map >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Karte (STL/CLR)](../dotnet/map-stl-clr.md)   
 [Map:: Find (STL/CLR)](../dotnet/map-find-stl-clr.md)   
 [map::insert (STL/CLR)](../dotnet/map-insert-stl-clr.md)