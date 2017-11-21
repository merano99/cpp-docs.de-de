---
title: 'priority_queue:: size_type (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::priority_queue::size_type
dev_langs: C++
helpviewer_keywords: size_type member [STL/CLR]
ms.assetid: 0f38e670-4f61-474a-990c-0b8cd31ada5e
caps.latest.revision: "13"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 6e98c9c180bb376032eb8ec74e431ba5408af3f9
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="priorityqueuesizetype-stlclr"></a>priority_queue::size_type (STL/CLR)
Der Typ eines Abstands mit Vorzeichen zwischen zwei Elementen.  
  
## <a name="syntax"></a>Syntax  
  
```  
typedef int size_type;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Typ beschreibt ein nicht negativer Elementanzahl.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_priority_queue_size_type.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::priority_queue<wchar_t> Mypriority_queue;   
int main()   
    {   
    Mypriority_queue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// compute positive difference   
    Mypriority_queue::size_type diff = c1.size();   
    c1.pop();   
    c1.pop();   
    diff -= c1.size();   
    System::Console::WriteLine("size difference = {0}", diff);   
    return (0);   
    }  
  
```  
  
```Output  
 c a b  
size difference = 2  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext bzw. einer neuen Warteschlange >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Priority_queue (STL/CLR)](../dotnet/priority-queue-stl-clr.md)   
 [priority_queue::empty (STL/CLR)](../dotnet/priority-queue-empty-stl-clr.md)