---
title: 'Übersetzung: Diagnose'
ms.date: 11/04/2016
ms.assetid: 3730ca7c-0147-452d-bd4a-6a1e97e9793e
ms.openlocfilehash: 4863b97dc1db7ff295b5f786ca97da2551d0fa62
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50664996"
---
# <a name="translation-diagnostics"></a>Übersetzung: Diagnose

**ANSI 2.1.1.3** Wie eine Diagnose identifiziert wird

Microsoft C erzeugt Fehlermeldungen in der Form:

> *filename* **(** *line-number* **) :** *diagnostic* **C**<em>number</em> *message*

Hierbei ist *filename* der Name der Quelldatei, in der der Fehler aufgetreten ist; *line-number* die Nummer der Zeile, in der der Compiler den Fehler festgestellt hat; *diagnostic* entweder „error“ oder „warning“; *number* eine eindeutige vierstellige Zahl (der ein **C** vorangestellt ist, wie in der Syntax kenntlich gemacht), die den Fehler bzw. die Warnung angibt, und *message* eine erläuternde Meldung.

## <a name="see-also"></a>Siehe auch

[Implementation-Defined Behavior (Durch die Implementierung definiertes Verhalten)](../c-language/implementation-defined-behavior.md)