---
title: Spezifizierer | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- declaration specifiers
- declarations, specifiers
- specifiers, in declarations
ms.assetid: 8b14e844-9880-4571-8779-28c8efe44633
caps.latest.revision: 9
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: c67ae6ce353ee48635df1b3be6b124344cdd4e91
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="specifiers"></a>Spezifizierer
In diesem Thema wird beschrieben, die *Decl-Specifiers* (deklarationsspezifizierer) Bestandteil einer [Deklaration](declarations-and-definitions-cpp.md).  
  
 Die folgenden Platzhalter und Sprachschlüsselwörter sind Deklarationsbezeichner:  
  
 *Storage-Class-specifier*  
  
 *Typspezifizierer*  
  
 *Funktion-Spezifizierer*  
  
 ["Friend"](../cpp/friend-cpp.md)  
  
 [typedef](http://msdn.microsoft.com/en-us/cc96cf26-ba93-4179-951e-695d1f5fdcf1)  
  
 [__declspec](../cpp/declspec.md) `(` *extended-Decl-Modifier-Seq*`)`  
  
## <a name="remarks"></a>Hinweise  
 Die *Decl-Specifiers* Teil einer Deklaration ist die längste Sequenz von *Decl-Specifiers* , der als Typname, nicht einschließlich des Zeigers oder verweismodifizierer erstellt werden können. Der Rest der Deklaration ist die *Deklarator*, der den eingeführten Namen enthält.  
  
 Die folgende Tabelle enthält vier Deklarationen und listet dann jede Deklaration *Decl-Specifers* und *Deklarator* Komponente getrennt.  
  
|Deklaration|*Decl-specifiers*|`declarator`|  
|-----------------|------------------------|------------------|  
|`char *lpszAppName;`|`char`|`*lpszAppName`|  
|`typedef char * LPSTR;`|`char`|`*LPSTR`|  
|`const int func1();`|`const int`|`func1`|  
|`volatile void *pvvObj;`|`volatile void`|`*pvvObj`|  
  
 Da `signed`, `unsigned`, `long`, und `short` alle implizieren `int`, `typedef` name, der eines dieser Schlüsselwörter stammt, ein Mitglied sein *Declarator-List* nicht der *Decl-Specifiers*.  
  
> [!NOTE]
>  Da ein Name neu deklariert werden kann, unterliegt seine Interpretation der letzten Deklaration im aktuellen Gültigkeitsbereich. Eine Neudeklaration kann beeinflussen, wie Namen vom Compiler interpretiert werden, insbesondere `typedef`-Namen.  
  
## <a name="see-also"></a>Siehe auch  
 [Deklarationen und Definitionen](declarations-and-definitions-cpp.md)