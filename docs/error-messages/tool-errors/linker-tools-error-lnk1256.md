---
title: Linkertoolfehler Lnk1256 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- xml
- LNK1256
dev_langs:
- C++
helpviewer_keywords:
- LNK1256
ms.assetid: 55b64b2b-a56b-436c-a55e-ec9c6dcb050e
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: 5e29e6100b57531c7a29f84e7c0feac53f20cec9
ms.contentlocale: de-de
ms.lasthandoff: 04/01/2017

---
# <a name="linker-tools-error-lnk1256"></a>Linkertoolfehler LNK1256
Fehler bei ALINK-Operation: Ursache  
  
 Ein häufiger Grund für LNK1256 ist eine falsche Versionsnummer für eine Assembly. Der Wert 65535 ist für keinen Teil der Assemblyversionsnummer zulässig. Der gültige Bereich für Assemblyversionen ist 0 – 65534.  
  
 LNK1256 kann auch entstehen, wenn ALINK den benannten Schlüsselcontainer nicht finden konnte. Container für den Schlüssel löschen und erneut hinzufügen zum CSP für starke Namen mit [Sn.exe (Strong Name-Tool)](http://msdn.microsoft.com/Library/c1d2b532-1b8e-4c7a-8ac5-53b801135ec6).  
  
 Ein weiterer Grund für LNK1256 ist ein Versionskonflikt zwischen dem Linker und Alink.dll. Dies kann durch eine fehlerhafte Installation von Visual Studio verursacht werden. Verwendung **Programme und Funktionen** in der Windows-Systemsteuerung reparieren oder neu installieren von Visual Studio.  
  
 Im folgende Beispiel wird LNK1256 generiert:  
  
```  
// LNK1256.cpp  
// compile with: /clr /LD  
// LNK1256 expected  
[assembly:System::Reflection::AssemblyVersionAttribute("1.0.65535")];  
public class CMyClass {  
public:  
   int value;  
};  
```