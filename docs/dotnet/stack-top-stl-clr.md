---
title: "stack::top (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::stack::top"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "top-Member [STL/CLR]"
ms.assetid: 5d8b7b69-336e-4d01-8b91-413a17aa2533
caps.latest.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# stack::top (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Greift auf das letzte Element zu.  
  
## Syntax  
  
```  
reference top();  
```  
  
## Hinweise  
 Die Memberfunktion gibt einen Verweis auf das letzte Element der gesteuerten Sequenz zurück, die nicht leer sein muss.  Sie verwenden sie, um auf das letzte Element zugreifen, wenn Sie wissen, dass es vorhanden ist.  
  
## Beispiel  
  
```  
// cliext_stack_top.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect last item   
    System::Console::WriteLine("top() = {0}", c1.top());   
  
// alter last item and reinspect   
    c1.top() = L'x';   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **ein b c**  
**top\(\) \= c**  
 **ein b x**   
## Anforderungen  
 **Header:** \<cliext\/Stapel\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [Stapel](../dotnet/stack-stl-clr.md)   
 [stack::top\_item](../dotnet/stack-top-item-stl-clr.md)