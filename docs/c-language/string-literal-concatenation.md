---
title: Zeichenfolgenliteralverkettung | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- concatenating strings
- strings [C++], concatenating
ms.assetid: 51486b1f-4b1e-4061-9add-1aa38c6cdb3c
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 5974e192e32c612fe995cbc736e703f6168a3e8d
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="string-literal-concatenation"></a>Zeichenfolgenliteral-Verkettung
Um Zeichenfolgenliterale zu bilden, die mehr als eine Zeile umfassen, können Sie die beiden Zeichenfolgen verketten. Geben Sie dazu einen umgekehrten Schrägstrich ein, und drücken Sie die EINGABETASTE. Der umgekehrte Schrägstrich bewirkt, dass der Compiler das folgende Zeilenumbruchszeichen ignoriert. Beispielweise ist das Zeichenfolgenliteral  
  
```  
"Long strings can be bro\  
ken into two or more pieces."  
```  
  
 identisch mit der Zeichenfolge  
  
```  
"Long strings can be broken into two or more pieces."  
```  
  
 Die Zeichenfolgenverkettung kann überall dort verwendet werden, wo Sie zuvor einen umgekehrten Schrägstrich gefolgt von einer Zeilenendemarke verwendet haben, um Zeichenfolgen einzugeben, die länger als eine Zeile sind.  
  
 Um eine neue Zeile innerhalb eines Zeichenfolgenliterals zu erzwingen, geben Sie die Escapesequenz für den Zeilenumbruch (**\n**) nach dem folgenden Muster in der Zeichenfolge ein, in der der Zeilenumbruch erstellt werden soll:  
  
```  
"Enter a number between 1 and 100\nOr press Return"  
```  
  
 Da Zeichenfolgen in jeder Spalte des Quellcodes beginnen und lange Zeichenfolgen in jeder Spalte einer Folgezeile fortgesetzt werden können, können Sie Zeichenfolgen positionieren, um die Lesbarkeit des Quellcodes zu verbessern. In jedem Fall ihre Darstellung auf dem Bildschirm, wenn die Ausgabe nicht betroffen ist. Zum Beispiel:  
  
```  
printf_s ( "This is the first half of the string, "  
           "this is the second half ") ;  
```  
  
 Solange jeder Teil der Zeichenfolge in doppelte Anführungszeichen eingeschlossen ist, werden die Teile als eine einzelne Zeichenfolge verkettet und ausgegeben. Diese Verkettung erfolgt gemäß der Sequenz von Ereignissen während der Kompilierung, die von [Übersetzungsphasen](../preprocessor/phases-of-translation.md) angegeben wird.  
  
```  
"This is the first half of the string, this is the second half"  
```  
  
 Ein Zeichenfolgenzeiger, der als zwei unterschiedliche Zeichenfolgenliterale initialisiert ist, die nur durch Leerraum getrennt sind, wird als eine einzelne Zeichenfolge gespeichert (Zeiger werden in [Zeigerdeklarationen](../c-language/pointer-declarations.md) erläutert). Bei ordnungsgemäßem Verweisen, wie im folgenden Beispiel, ist das Ergebnis mit dem vorherigen Beispiel identisch:  
  
```  
char *string = "This is the first half of the string, "  
               "this is the second half";  
  
printf_s( "%s" , string ) ;  
```  
  
 In Übersetzungsphase 6 werden die Mehrbytezeichensequenzen, die von einer beliebigen Folge von angrenzenden Zeichenfolgenliteralen oder angrenzenden breiten Zeichenfolgenliteralen angegeben werden, in einer einzelnen Mehrbytezeichensequenz verkettet. Entwerfen Sie daher keine Programme, um Änderungen von Zeichenfolgenliteralen während der Ausführung zu ermöglichen. Der ANSI C-Standard gibt an, dass das Ergebnis der Änderung einer Zeichenfolge nicht definiert ist.  
  
## <a name="see-also"></a>Siehe auch  
 [C-Zeichenfolgenliterale](../c-language/c-string-literals.md)