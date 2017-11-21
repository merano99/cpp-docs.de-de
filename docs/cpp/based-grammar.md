---
title: __based-Grammatik | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
helpviewer_keywords: based addressing
ms.assetid: a68ff750-c7fa-4c0c-8d5f-2df76e4686c5
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: abcaa55bb0453b894f4023a68743f570bc6c3c52
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="based-grammar"></a>__based-Grammatik
## <a name="microsoft-specific"></a>Microsoft-spezifisch  
 Die basierende Adressierung ist nützlich, wenn eine genaue Kontrolle über das Segment erforderlich ist, in dem Objekte zugeordnet sind (statische und dynamische basierende Daten).  
  
 Die einzige Form der basierenden Adressierung, die in 32-Bit- und 64-Bit-Kompilierungen zulässig ist "basiert auf einem Zeiger". Dieser gibt einen Typ an, der eine 32-Bit- oder 64-Bit-Verschiebung auf eine 32-Bit- oder 64-Bit-Basis enthält oder auf `void` basiert.  
  
## <a name="grammar"></a>Grammatik  
 *Basis-Range-Modifizierer*:  
 **__based (***Base Ausdruck***)**   
  
 *Basis-Expression*:  
 *based-variablebased-abstract-declaratorsegment-namesegment-CAST*  
  
 *Basis-Variable*:  
 *identifier*  
  
 *Basis-Abstract-Declarator*:  
 *Abstract-declarator*  
  
 *Basistyp*:  
 *Typname*  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Basierte Zeiger](../cpp/based-pointers-cpp.md)