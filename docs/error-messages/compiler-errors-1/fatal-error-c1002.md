---
title: Schwerwiegender Fehler C1002
ms.date: 11/04/2016
f1_keywords:
- C1002
helpviewer_keywords:
- C1002
ms.assetid: bd6d274a-c7b4-43af-8bf2-23c5e442aa22
ms.openlocfilehash: 0588da99994be547742cc530ba435002a2d73359
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50640504"
---
# <a name="fatal-error-c1002"></a>Schwerwiegender Fehler C1002

Im 2. Durchlauf ist kein Heapspeicher mehr für den Compiler verfügbar.

Der Compiler war nicht genügend Speicherplatz für dynamischen Arbeitsspeicher während des zweiten Durchlaufs, wahrscheinlich aufgrund eines Programms durch zu viele Symbole oder komplexe Ausdrücke.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>So beheben Sie den Fehler (unterschiedliche Lösungsmöglichkeiten)

1. Unterteilen Sie die Quelldatei, in mehreren kleineren Dateien.

1. Unterteilen Sie Ausdrücke in kleinere Teilausdrücke an.

1. Entfernen Sie andere Programme oder Treiber, die Speicher belegen.