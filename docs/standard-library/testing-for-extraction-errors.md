---
title: "Überprüfen von Extraktionen | Microsoft-Dokumentation"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: extraction errors
ms.assetid: 6a681028-adba-4557-8f7b-f137932905f8
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 088cc150513d593aff5d4250c899eb3712c5fe39
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="testing-for-extraction-errors"></a>Überprüfen von Extraktionen
Verarbeitungsfunktionen für Ausgabefehler, die unter [Fehlerverarbeitende Funktionen](../standard-library/output-file-stream-member-functions.md) erörtert wurden, sind für Eingabestreams relevant. Das Testen auf Fehler ist während der Extraktion wichtig. Berücksichtigen Sie Folgendes:  
  
```  
cin>> n;  
```  
  
 Wenn `n` eine Ganzzahl mit Vorzeichen ist, legt ein Wert größer als 32.767 (der maximal zulässige Wert oder MAX_INT) das `fail`-Bit des Streams fest, und das `cin`-Objekt kann nicht mehr verwendet werden. Alle nachfolgenden Extraktionen führen zu einer sofortigen Rückgabe ohne gespeicherten Wert.  
  
## <a name="see-also"></a>Siehe auch  
 [Eingabestreams](../standard-library/input-streams.md)
