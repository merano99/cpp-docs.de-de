---
title: "multimap::multimap (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::multimap::multimap"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "multimap-Member [STL/CLR]"
ms.assetid: cdf9c5dc-774c-424e-aeea-7554643e401c
caps.latest.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# multimap::multimap (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Erstellt ein container\-Objekt.  
  
## Syntax  
  
```  
multimap();  
explicit multimap(key_compare^ pred);  
multimap(multimap<Key, Mapped>% right);  
multimap(multimap<Key, Mapped>^ right);  
template<typename InIter>  
    multimapmultimap(InIter first, InIter last);  
template<typename InIter>  
    multimap(InIter first, InIter last,  
        key_compare^ pred);  
multimap(System::Collections::Generic::IEnumerable<GValue>^ right);  
multimap(System::Collections::Generic::IEnumerable<GValue>^ right,  
    key_compare^ pred);  
```  
  
#### Parameter  
 first  
 Anfang Einfügen des Bereichs.  
  
 last  
 Ende Einfügen des Bereichs.  
  
 pred  
 Reihenfolgenprädikat für die gesteuerte Sequenz.  
  
 right  
 Objekt oder Bereich Einfüge\-.  
  
## Hinweise  
 Der Konstruktor:  
  
 `multimap();`  
  
 initialisiert die gesteuerte Sequenz ohne Elemente, mit dem Standardreihenfolgenprädikat `key_compare()`.  Sie verwenden sie, um eine leere gesteuerten ursprünglichen Sequenz, mit dem Standardreihenfolgenprädikat anzugeben.  
  
 Der Konstruktor:  
  
 `explicit multimap(key_compare^ pred);`  
  
 initialisiert die gesteuerte Sequenz ohne Elemente, mit dem Reihenfolgenprädikat `pred`.  Sie verwenden sie, um eine leere gesteuerten ursprünglichen Sequenz, mit dem angegebenen Reihenfolgenprädikat anzugeben.  
  
 Der Konstruktor:  
  
 `multimap(multimap<Key, Mapped>% right);`  
  
 initialisiert die gesteuerte Sequenz mit der Sequenz `[``right``.`[multimap::begin](../dotnet/multimap-begin-stl-clr.md)`(),` `right``.`[multimap::end](../dotnet/multimap-end-stl-clr.md)`())`, mit dem Standardreihenfolgenprädikat.  Sie verwenden sie, um einer gesteuerten ursprünglichen Sequenz, die eine Kopie der Sequenz, die erfolgen durch das multimap\-Objekt `right` gesteuert wird, mit dem Standardreihenfolgenprädikat anzugeben.  
  
 Der Konstruktor:  
  
 `multimap(multimap<Key, Mapped>^ right);`  
  
 initialisiert die gesteuerte Sequenz mit der Sequenz `[``right``->`[multimap::begin](../dotnet/multimap-begin-stl-clr.md)`(),` `right``->`[multimap::end](../dotnet/multimap-end-stl-clr.md)`())`, mit dem Standardreihenfolgenprädikat.  Sie verwenden sie, um einer gesteuerten ursprünglichen Sequenz, die eine Kopie der Sequenz, die erfolgen durch das multimap\-Objekt `right` gesteuert wird, mit dem Standardreihenfolgenprädikat anzugeben.  
  
 Der Konstruktor:  
  
 `template<typename InIter>`  
  
 `multimap(InIter first, InIter last);`  
  
 initialisiert die gesteuerte Sequenz mit der Sequenz `[``first``,` `last``)`, mit dem Standardreihenfolgenprädikat.  Sie verwenden sie, um die gesteuerte Sequenz eine Kopie einer anderen Sequenz, mit dem Standardreihenfolgenprädikat zu erstellen.  
  
 Der Konstruktor:  
  
 `template<typename InIter>`  
  
 `multimap(InIter first, InIter last,`  
  
 `key_compare^ pred);`  
  
 initialisiert die gesteuerte Sequenz mit der Sequenz `[``first``,` `last``)`, mit dem Reihenfolgenprädikat `pred`.  Sie verwenden sie, um die gesteuerte Sequenz eine Kopie einer anderen Sequenz, mit dem angegebenen Reihenfolgenprädikat zu erstellen.  
  
 Der Konstruktor:  
  
 `multimap(System::Collections::Generic::IEnumerable<Key>^ right);`  
  
 initialisiert die gesteuerte Sequenz mit der Folge, die der Enumerator `right`, mit dem Standardreihenfolgenprädikat festgelegt wird.  Sie verwenden sie, um die gesteuerte Sequenz eine Kopie einer anderen Sequenz erstellen, die von ein Enumerator, mit dem Standardreihenfolgenprädikat beschrieben wird.  
  
 Der Konstruktor:  
  
 `multimap(System::Collections::Generic::IEnumerable<Key>^ right,`  
  
 `key_compare^ pred);`  
  
 initialisiert die gesteuerte Sequenz mit der Folge, die der Enumerator `right`, mit dem Reihenfolgenprädikat `pred` festgelegt wird.  Sie verwenden sie, um die gesteuerte Sequenz eine Kopie einer anderen Sequenz erstellen, die von ein Enumerator, mit dem angegebenen Reihenfolgenprädikat beschrieben wird.  
  
## Beispiel  
  
```  
// cliext_multimap_construct.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
int main()   
    {   
// construct an empty container   
    Mymultimap c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
    c1.insert(Mymultimap::make_value(L'a', 1));   
    c1.insert(Mymultimap::make_value(L'b', 2));   
    c1.insert(Mymultimap::make_value(L'c', 3));   
    for each (Mymultimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an ordering rule   
    Mymultimap c2 = cliext::greater_equal<wchar_t>();   
    System::Console::WriteLine("size() = {0}", c2.size());   
  
    c2.insert(c1.begin(), c1.end());   
    for each (Mymultimap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an iterator range   
    Mymultimap c3(c1.begin(), c1.end());   
    for each (Mymultimap::value_type elem in c3)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an iterator range and an ordering rule   
    Mymultimap c4(c1.begin(), c1.end(),   
        cliext::greater_equal<wchar_t>());   
    for each (Mymultimap::value_type elem in c4)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an enumeration   
    Mymultimap c5(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<   
            Mymultimap::value_type>^)%c3);   
    for each (Mymultimap::value_type elem in c5)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an enumeration and an ordering rule   
    Mymultimap c6(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<   
            Mymultimap::value_type>^)%c3,   
                cliext::greater_equal<wchar_t>());   
    for each (Mymultimap::value_type elem in c6)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct by copying another container   
    Mymultimap c7(c4);   
    for each (Mymultimap::value_type elem in c7)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct by copying a container handle   
    Mymultimap c8(%c3);   
    for each (Mymultimap::value_type elem in c8)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **size\(\) \= 0**  
 **\[1\] \[2\] \[bc 3\]**  
**size\(\) \= 0**  
 **c \[3\] \[2\] \[b1\]**  
 **\[1\] \[2\] \[bc 3\]**  
 **c \[3\] \[2\] \[b1\]**  
 **\[1\] \[2\] \[bc 3\]**  
 **c \[3\] \[2\] \[b1\]**  
 **c \[3\] \[2\] \[b1\]**  
 **\[1\] \[2\] \[bc 3\]**   
## Anforderungen  
 **Header:** \<cliext\/Zuordnung\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [multimap](../dotnet/multimap-stl-clr.md)   
 [multimap::generic\_container](../dotnet/multimap-generic-container-stl-clr.md)   
 [multimap::operator\=](../dotnet/multimap-operator-assign-stl-clr.md)