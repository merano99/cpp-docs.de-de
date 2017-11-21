---
title: "C-Ausdrücke (konstant) | Microsoft-Dokumentation"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- constant expressions, syntax
- constant expressions
- expressions [C++], constant
ms.assetid: d48a6c47-e44c-4be2-9c8b-7944c7ef8de7
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: e7b9beac4d87e0580279190cca005fc56c951af8
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="c-constant-expressions"></a>C-Ausdrücke (konstant)
Ein konstanter Ausdruck wird zur Kompilierzeit, nicht zur Laufzeit, ausgewertet und kann an einem beliebigen Ort verwendet werden, an dem eine Konstante verwendet werden kann. Der konstante Ausdruck muss eine Konstante auswerten, die sich im Bereich der darstellbaren Werte für diesen Typ befindet. Die Operanden eines konstanten Ausdrucks können ganzzahlige Konstanten, Zeichenkonstanten, Gleitkommakonstanten, Enumerationskonstanten, Typumwandlungen, `sizeof`-Ausdrücke und andere konstante Ausdrücke sein.  
  
## <a name="syntax"></a>Syntax  
 *constant-expression*:  
 *conditional-expression*  
  
 *conditional-expression*:  
 *logical-OR-expression*  
  
 *logical-OR-expression* **?**  *expression* **:**  *conditional-expression*  
  
 *expression*:  
 *assignment-expression*  
  
 *expression* **,**  *assignment-expression*  
  
 *assignment-expression*:  
 *conditional-expression*  
  
 *unary-expression assignment-operator assignment-expression*  
  
 *assignment-operator*: Einer von  
 **= \*= /= %= += -= <\<= >>= &= ^= &#124;=**  
  
 Die Nichtterminalen für den Strukturdeklarator, den Enumerator, den direkten Deklarator, den direkt-abstrakten Deklarator und die gekennzeichnete Anweisung enthalten das Nichtterminal *constant-expression*.  
  
 Ein ganzzahliger konstanter Ausdruck muss verwendet werden, um die Größe eines Bitfeldmembers einer Struktur, den Wert einer Enumerationskonstanten, die Größe eines Arrays oder den Wert einer **case**-Konstanten anzugeben.  
  
 Konstante Ausdrücke, die in den Präprozessoranweisungen verwendet werden, unterliegen zusätzlichen Einschränkungen. Daher sind sie als "eingeschränkte konstante Ausdrücke" bekannt. Ein eingeschränkter konstanter Ausdruck kann keine `sizeof`-Ausdrücke, Enumerationskonstanten, Typumwandlungen zu keinem Typ oder Float-Konstanten enthalten. Er kann jedoch den speziellen konstanten Ausdruck `defined (`*identifier*`)` enthalten.  
  
## <a name="see-also"></a>Siehe auch  
 [Operanden und Ausdrücke](../c-language/operands-and-expressions.md)