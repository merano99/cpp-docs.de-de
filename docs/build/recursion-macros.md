---
title: Rekursionsmakros
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, recursion macros
- recursion macros
- macros, recursion
ms.assetid: c53e5ae7-619e-46b1-bdc2-86d8c7798b1d
ms.openlocfilehash: 0005a4be0422ed83816eabc7b55932a81441ae25
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50451258"
---
# <a name="recursion-macros"></a>Rekursionsmakros

Verwenden Sie Rekursionsmakros NMAKE rekursiv aufgerufen. Rekursive Sitzungen erben Befehlszeilen- und Umgebungsvariablen-Makros und Tools.ini Informationen. Sie erben nicht die Makefile-definierte Rückschlussregeln oder **. SUFFIXE** und **. WERTVOLLE** Spezifikationen. Um eine rekursive NMAKE-Sitzung Makros übergeben, legen Sie eine Umgebungsvariable mit vor dem rekursiven Aufruf, definieren Sie ein Makro im Befehl für den rekursiven Aufruf, oder definieren Sie ein Makro in Tools.ini.

|Makro|Definition|
|-----------|----------------|
|**STELLEN**|Befehl, der ursprünglich zum Aufrufen von NMAKE verwendet.<br /><br /> Das $(make)-makro gibt den vollständigen Pfad zu nmake.exe.|
|**MAKEDIR**|Aktuelle Verzeichnis beim Aufruf von NMAKE.|
|**MAKEFLAGS**|Die Optionen momentan. Verwenden Sie als `/$(MAKEFLAGS)`.  Beachten Sie, dass/f nicht enthalten ist.|

## <a name="see-also"></a>Siehe auch

[Besondere NMAKE-Makros](../build/special-nmake-macros.md)