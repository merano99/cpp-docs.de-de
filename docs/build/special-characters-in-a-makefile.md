---
title: Sonderzeichen in einem Makefile | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- NMAKE program, special characters
- makefiles, special characters
- special characters, in NMAKE macros
- macros, special characters
ms.assetid: 92c34ab5-ca6b-4fc0-bcf4-3172eaeda9f0
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 53b2457c87e587b4e1ef13e53bf2dfcdd4800d7f
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="special-characters-in-a-makefile"></a>Sonderzeichen in einem Makefile
Um eine besondere NMAKE-Zeichen als Literalzeichen zu verwenden, platzieren Sie ein Caretzeichen (^) davor. NMAKE ignoriert Caretzeichen, die andere Zeichen sind. Sonderzeichen sind:  
  
 `:  ;  #  (  )  $  ^  \  {  }  !  @  —`  
  
 Ein Caretzeichen (^) innerhalb einer Zeichenfolge in Anführungszeichen wird als literales Zirkumflexzeichen behandelt. Eine Einfügemarke am Ende einer Zeile Fügt ein literal neue Zeilenumbruchzeichen in eine Zeichenfolge oder ein Makro.  
  
 In Makros, einen umgekehrten Schrägstrich (\\) gefolgt durch einen Zeilenvorschub Zeichen wird durch ein Leerzeichen ersetzt.  
  
 Bei Befehlen wird ein Prozentzeichen (%) den Dateibezeichner. Um dieses Zeichen in einem Befehl darzustellen, geben Sie ein doppelten Prozentzeichen (%) anstelle einer einzigen. In anderen Situationen interpretiert NMAKE ein einzelnes % buchstäblich, aber es wird immer ein Double-Wert interpretiert %% als ein einzelnes %. Aus diesem Grund, um ein Literal darzustellen %%, geben Sie entweder drei Prozentzeichen %%%, oder vier Prozentzeichen, %%%.  
  
 Um das Dollarzeichen ($) als Literalzeichen in einem Befehl zu verwenden, geben Sie zwei Dollarzeichen ($$). Diese Methode kann auch verwendet werden, in anderen Situationen, in denen ^ $ funktioniert.  
  
## <a name="see-also"></a>Siehe auch  
 [Inhalt eines Makefiles](../build/contents-of-a-makefile.md)