---
title: hash_set::make_value (STL/CLR) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_set::make_value
dev_langs: C++
helpviewer_keywords: make_value member [STL/CLR]
ms.assetid: 19819fee-d3a0-428d-92db-cba7235d37d4
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 3a34387a274cc1d804c74dcb086f667791f5e16f
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="hashsetmakevalue-stlclr"></a>hash_set::make_value (STL/CLR)
Erstellt ein Wertobjekt.  
  
## <a name="syntax"></a>Syntax  
  
```  
static value_type make_value(key_type key);  
```  
  
#### <a name="parameters"></a>Parameter  
 Key  
 Schlüsselwert verwenden.  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt eine `value_type` Objekts, dessen Schlüssel `key`. Sie verwenden es, um ein Objekt, das für die Verwendung mit anderen Memberfunktionen geeignet zu verfassen.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_set_make_value.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    c1.insert(Myhash_set::make_value(L'a'));   
    c1.insert(Myhash_set::make_value(L'b'));   
    c1.insert(Myhash_set::make_value(L'c'));   
  
// display contents " a b c"   
    for each (Myhash_set::value_type elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_set/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Hash_set (STL/CLR)](../dotnet/hash-set-stl-clr.md)   
 [hash_set:: KEY_TYPE (STL/CLR)](../dotnet/hash-set-key-type-stl-clr.md)   
 [hash_set::value_type (STL/CLR)](../dotnet/hash-set-value-type-stl-clr.md)