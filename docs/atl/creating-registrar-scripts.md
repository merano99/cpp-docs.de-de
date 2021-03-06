---
title: Erstellen von Skripts für ATL-Registrierung
ms.date: 11/04/2016
helpviewer_keywords:
- scripting, registry scripting
- ATL, registry
- registrar scripts [ATL]
- scripts, Registrar scripts
- scripts, creating
ms.assetid: cbd5024b-8061-4a71-be65-7fee90374a35
ms.openlocfilehash: bc76e41ab0d2cd2d26ef227e6368cb420a8a6401
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50480237"
---
# <a name="creating-registrar-scripts"></a>Creating Registrar Scripts

Ein Skript für die Registrierungsstelle bietet datengesteuerten, anstatt API-gesteuert, auf die Registrierung des Systems. Datengesteuerte Zugriff ist in der Regel effizienter, da es nur ein oder zwei Zeilen in einem Skript Hinzufügen eines Schlüssels in der Registrierung kann.

Die [ATL-Steuerelement-Assistent](../atl/reference/atl-control-wizard.md) generiert automatisch ein Skript Registrierungsstelle für Ihren COM-Server. Dieses Skript finden Sie in der RGS-Datei mit dem Objekt verknüpft ist.

Der ATL-Registrierung-Skript-Engine verarbeitet Ihre Registrierungsstelle-Skripts zur Laufzeit. ATL wird automatisch der Skript-Engine während der Server-Setup aufgerufen.

In diesem Artikel werden die folgenden Themen im Zusammenhang mit der Registrierungsstelle Skripts behandelt:

- [Einführung in die BNF-Snytax (Backus Naur Form)](../atl/understanding-backus-nauer-form-bnf-syntax.md)

- [Einführung in Analysestrukturen](../atl/understanding-parse-trees.md)

- [Beispiele für die Registrierungsskripterstellung](../atl/registry-scripting-examples.md)

- [Verwenden von ersetzbaren Parametern (Der Registrierungspräprozessor)](../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md)

- [Aufruf von Skripts](../atl/invoking-scripts.md)

## <a name="see-also"></a>Siehe auch

[Registrierungskomponente (Registrar)](../atl/atl-registry-component-registrar.md)

