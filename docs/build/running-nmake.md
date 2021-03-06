---
title: Ausführen von NMAKE
ms.date: 09/05/2018
helpviewer_keywords:
- targets, building
- response files, NMAKE
- targets
- command files
- NMAKE program, targets
- NMAKE program, running
- command files, NMAKE
ms.assetid: 0421104d-8b7b-4bf3-86c1-928d9b7c1a8c
ms.openlocfilehash: 81f38792893955b476dfc7eda91ed00603924a8f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50646211"
---
# <a name="running-nmake"></a>Ausführen von NMAKE

## <a name="syntax"></a>Syntax

> **NMAKE:** [*Option* ...] [*Makros* ...] [*Ziele* ...] [**\@**<em>Commandfile</em> ...]

## <a name="remarks"></a>Hinweise

NMAKE-Builds, die nur angegebenen *Ziele* oder, wenn keine Angabe erfolgt, wird die erste in das Makefile Ziel. Das erste Makefileziel möglich einen [Pseudoziel](../build/pseudotargets.md) , das anderen Zielen erstellt. NMAKE verwendet Makefiles, die mit/f angegeben. Wenn/f nicht angegeben ist, wird die Makefile-Datei im aktuellen Verzeichnis. Wenn kein Makefile angegeben ist, verwendet es Rückschlussregeln zum Erstellen von Befehlszeilen *Ziele*.

Die *Commandfile* -Text-Datei (oder Antwortdatei) enthält die Befehlszeileneingabe. Vor oder nach einem anderen Eingaben \@ *Commandfile*. Ein Pfad ist zulässig. In *Commandfile*, Zeilenumbrüche werden als Leerzeichen behandelt. Schließen Sie Makrodefinitionen in Anführungszeichen ein, wenn diese Leerzeichen enthalten.

## <a name="what-do-you-want-to-know-more-about"></a>Worüber möchten Sie mehr erfahren?

[NMAKE-Optionen](../build/nmake-options.md)

[Tools.ini und NMAKE](../build/tools-ini-and-nmake.md)

[Exitcodes von NMAKE](../build/exit-codes-from-nmake.md)

## <a name="see-also"></a>Siehe auch

[NMAKE-Referenz](../build/nmake-reference.md)