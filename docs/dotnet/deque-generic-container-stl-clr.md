---
title: "deque::generic_container (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::deque::generic_container"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "generic_container-Member [STL/CLR]"
ms.assetid: 5003a9a8-c207-4074-be2b-36cb9887f9d4
caps.latest.revision: 17
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 15
---
# deque::generic_container (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Der Typ der generischen Schnittstelle für den Container.  
  
## Syntax  
  
```  
typedef Microsoft::VisualC::StlClr::  
    IDeque<generic_value>  
    generic_container;  
```  
  
## Hinweise  
 Der Typ beschreibt die generische Schnittstelle für diese Vorlagencontainerklasse.  
  
## Beispiel  
  
```  
// cliext_deque_generic_container.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct a generic container   
    cliext::deque<wchar_t>::generic_container^ gc1 = %c1;   
    for each (wchar_t elem in gc1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// modify generic and display original   
    gc1->insert(gc1->end(), L'd');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// modify original and display generic   
    c1.push_back(L'e');   
  
    System::Collections::IEnumerator^ enum1 =   
        gc1->GetEnumerator();   
    while (enum1->MoveNext())   
        System::Console::Write(" {0}", enum1->Current);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **ein b c**  
 **ein b c**  
 **ein b c d**  
 **ein b c d e**   
## Anforderungen  
 **Header:** \<cliext\/Doppelschlange\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 <xref:Microsoft.VisualC.StlClr.IDeque`1>   
 [deque](../dotnet/deque-stl-clr.md)   
 [deque::generic\_iterator](../dotnet/deque-generic-iterator-stl-clr.md)   
 [deque::generic\_reverse\_iterator](../dotnet/deque-generic-reverse-iterator-stl-clr.md)   
 [deque::generic\_value](../dotnet/deque-generic-value-stl-clr.md)