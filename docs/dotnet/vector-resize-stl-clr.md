---
title: 'Vector:: Resize (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::vector::resize
dev_langs: C++
helpviewer_keywords: resize member [STL/CLR]
ms.assetid: a3556fbc-67d9-463a-9ffc-cb43ee15657f
caps.latest.revision: "17"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 43616dbc6bf0cd0eca6493d4f474ce20d02b8e2d
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="vectorresize-stlclr"></a>vector::resize (STL/CLR)
Ändert die Anzahl der Elemente an.  
  
## <a name="syntax"></a>Syntax  
  
```  
void resize(size_type new_size);  
void resize(size_type new_size, value_type val);  
```  
  
#### <a name="parameters"></a>Parameter  
 new_size  
 Neue Größe der gesteuerten Sequenz.  
  
 Val  
 Der Wert des Elements Auffüllung.  
  
## <a name="remarks"></a>Hinweise  
 Die beiden Memberfunktionen sicher, dass [Vector:: Size (STL/CLR)](../dotnet/vector-size-stl-clr.md) `()` künftig gibt `new_size`. Wenn die gesteuerte Sequenz verlängert werden muss, fügt die erste Memberfunktion Elemente mit dem Wert `value_type()` an, während die zweite Memberfunktion Elemente mit dem Wert `val` anfügt. Um die gesteuerte Sequenz kürzere zu machen, beide Memberfunktionen effektiv das letzte Element löschen [Vector:: Size (STL/CLR)](../dotnet/vector-size-stl-clr.md) `() -` `new_size` Zeiten. Sie können damit stellen Sie sicher, dass die kontrollierte Sequenz Größe hat `new_size`, indem Sie verkürzen oder Auffüllen von der aktuellen gesteuerten Sequenz.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_vector_resize.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
// construct an empty container and pad with default values   
    cliext::vector<wchar_t> c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
    c1.resize(4);   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", (int)elem);   
    System::Console::WriteLine();   
  
// resize to empty   
    c1.resize(0);   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
// resize and pad   
    c1.resize(5, L'x');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
size() = 0  
 0 0 0 0  
size() = 0  
 x x x x x  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Vektor >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Vektor (STL/CLR)](../dotnet/vector-stl-clr.md)   
 [Vector:: Clear (STL/CLR)](../dotnet/vector-clear-stl-clr.md)   
 [Vector:: Erase (STL/CLR)](../dotnet/vector-erase-stl-clr.md)   
 [vector::insert (STL/CLR)](../dotnet/vector-insert-stl-clr.md)