---
title: "queue::assign (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::queue::assign"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "assign-Member [STL/CLR]"
ms.assetid: 5bec8a84-9561-43f7-ad7f-f845d0edef41
caps.latest.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 12
---
# queue::assign (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Ersetzt alle Elemente.  
  
## Syntax  
  
```  
void assign(queue<Value, Container>% right);  
```  
  
#### Parameter  
 right  
 Einzufügen Containeradapter.  
  
## Hinweise  
 Die Memberfunktion `right` weist `.get_container()` am zugrunde liegenden Container zu.  Sie verwenden sie, um den gesamten Inhalt der Warteschlange zu ändern.  
  
## Beispiel  
  
```  
// cliext_queue_assign.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::queue<wchar_t> Myqueue;   
int main()   
    {   
    Myqueue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign a repetition of values   
    Myqueue c2;   
    c2.assign(c1);   
    for each (wchar_t elem in c2.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **ein b c**  
 **ein b c**   
## Anforderungen  
 **Header:** \<cliext\/Warteschlange\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [queue](../dotnet/queue-stl-clr.md)   
 [queue::operator\=](../dotnet/queue-operator-assign-stl-clr.md)