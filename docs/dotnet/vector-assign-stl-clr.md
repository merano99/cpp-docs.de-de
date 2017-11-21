---
title: "vector::assign (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::vector::assign"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "assign-Member [STL/CLR]"
ms.assetid: 945e2048-6c61-4701-b13c-8241cbee3fa1
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# vector::assign (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Ersetzt alle Elemente.  
  
## Syntax  
  
```  
void assign(size_type count, value_type val);  
template<typename InIt>  
    void assign(InIt first, InIt last);  
void assign(System::Collections::Generic::IEnumerable<Value>^ right);  
```  
  
#### Parameter  
 count  
 Zahl einzufügen Elemente.  
  
 first  
 Anfang Einfügen des Bereichs.  
  
 last  
 Ende Einfügen des Bereichs.  
  
 right  
 Einzufügen Enumeration.  
  
 val  
 Wert des Elements eingefügt.  
  
## Hinweise  
 Die Memberfunktion die erste ersetzt gesteuerte Sequenz von einer Wiederholung von `count`\-Elemente des Werts `val`.  Sie verwenden sie, um den Container mit allen Elementen füllen, der denselben Wert verfügt.  
  
 Wenn `InIt` ein ganzzahliger Typ ist, verhält sich die zweite Memberfunktion genau wie `assign((size_type)``first``, (value_type)``last``)`.  Andernfalls ersetzt sie die gesteuerte Sequenz nach die Sequenz `[``first``,` `last``)`.  Sie verwenden sie, um die gesteuerte Sequenz eine Kopie erstellen einer anderen Sequenz.  
  
 Die dritte Memberfunktion ersetzt die gesteuerte Sequenz nach der Reihenfolge, die der Enumerator `right` festgelegt wird.  Sie verwenden sie, um die gesteuerte Sequenz eine Kopie einer Sequenz erstellen, die von ein Enumerator beschrieben wird.  
  
## Beispiel  
  
```  
// cliext_vector_assign.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// assign a repetition of values   
    cliext::vector<wchar_t> c2;   
    c2.assign(6, L'x');   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign an iterator range   
    c2.assign(c1.begin(), c1.end() - 1);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign an enumeration   
    c2.assign(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c1);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **x x x x x x**  
 **ein b**  
 **ein b c**   
## Anforderungen  
 **Header:** \<cliext\/Vektor\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [Vektor](../dotnet/vector-stl-clr.md)   
 [vector::operator\=](../dotnet/vector-operator-assign-stl-clr.md)