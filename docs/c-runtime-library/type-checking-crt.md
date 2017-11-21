---
title: "Typüberprüfung (CRT) | Microsoft-Dokumentation"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: c.types
dev_langs: C++
helpviewer_keywords:
- checking type
- variable argument functions
- type checking
ms.assetid: 1ba7590b-d1c0-4636-b6a0-e231395abdad
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 6bffc721ac685be91531b3d876234de8be2477c4
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="type-checking-crt"></a>Typüberprüfung (CRT)
Der Compiler führt eine beschränkte Typüberprüfung für Funktionen durch, die eine variable Anzahl von Argumenten aufnehmen können, wie im Folgenden beschrieben wird:  
  
|Funktionsaufruf |Typgeprüfte Argumente|  
|-------------------|-----------------------------|  
|`_cprintf_s`, `_cscanf_s`, `printf_s`, `scanf_s`|Erstes Argument (Formatzeichenfolge)|  
|`fprintf_s`, `fscanf_s`, `sprintf_s`, `sscanf_s`|Die ersten zwei Argumente (Datei oder Puffer und Formatzeichenfolge)|  
|`_snprintf_s`|Die ersten drei Argumente (Datei oder Puffer, Anzahl und Formatzeichenfolge)|  
|`_open`|Die ersten zwei Argumente (Pfad und `_open`-Flag)|  
|`_sopen_s`|Die ersten drei Argumente (Pfad, `_open`-Flag und Freigabemodus)|  
|`_execl`, `_execle`, `_execlp`, `_execlpe`|Die ersten zwei Argumente (Pfad und erster Argumentzeiger)|  
|`_spawnl`, `_spawnle`, `_spawnlp`, `_spawnlpe`|Die ersten drei Argumente (Moduskennzeichnung, Pfad und erster Argumentzeiger)|  
  
 Der Compiler führt dieselbe beschränkte Typüberprüfung für die äquivalenten Breitzeichen dieser Funktionen durch.  
  
## <a name="see-also"></a>Siehe auch  
 [CRT-Bibliotheksfunktionen](../c-runtime-library/crt-library-features.md)