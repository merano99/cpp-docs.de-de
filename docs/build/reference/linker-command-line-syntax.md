---
title: Syntax für die Linkerbefehlszeile
ms.date: 11/04/2016
helpviewer_keywords:
- linker [C++], syntax
- linker command line [C++]
- LINK tool [C++], command-line syntax
ms.assetid: e2a31e17-77bd-4e74-9305-75b105b26539
ms.openlocfilehash: 844d2fe4c02e274cda02fe71303f0b6dd092b431
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50464115"
---
# <a name="linker-command-line-syntax"></a>Syntax für die Linkerbefehlszeile

LINK zum Ausführen. EXE-Datei, verwenden Sie die folgende Befehlssyntax:

```
LINK arguments
```

Die `arguments` umfassen Optionen und Dateinamen ein, und können in beliebiger Reihenfolge angegeben werden. Optionen werden zuerst verarbeitet, und klicken Sie dann auf Dateien. Verwenden Sie eine oder mehrere Leerzeichen oder Tabstopps, um Argumente zu trennen.

> [!NOTE]
>  Sie können dieses Tool nur über die Visual Studio-Eingabeaufforderung starten. Sie können es nicht von einer Systemeingabeaufforderung oder vom Datei-Explorer aus starten.

In der Befehlszeile eine Option besteht aus einem Optionsbezeichner, entweder einen Bindestrich (-) oder einem Schrägstrich (/), gefolgt von den Namen der Option. Optionsnamen können nicht abgekürzt werden. Einige Optionen haben ein Argument, das nach einem Doppelpunkt (:) angegeben. Keine Leerzeichen oder Tabstopps sind innerhalb einer Optionsangabe, außer in eine Zeichenfolge in Anführungszeichen in der Option "/ Comment" zulässig. Geben Sie numerische Argumente, in Dezimalstellen oder C-Notation. Optionsnamen und ihren Argumenten-Schlüsselwort oder einen Dateinamen sind keine Groß-/Kleinschreibung beachtet, aber bestehenden Argumenten wird Groß-/Kleinschreibung beachtet.

Um eine Datei an dem Linker übergeben werden soll, geben Sie den Dateinamen in der Befehlszeile nach dem LINK-Befehl. Sie können einen absoluten oder relativen Pfad angeben, mit dem Dateinamen, und Sie können Platzhalter im Dateinamen verwenden. Wenn Sie den Punkt (.) und die Dateierweiterung weglassen, wird LINK obj für die Suche nach der Datei angenommen. LINK verwendet Dateinamenerweiterungen oder das Fehlen von ihnen keine Annahmen zum Inhalt der Dateien; Bestimmt den Typ der Datei durch Untersuchen und verarbeitet ihn entsprechend.

Link.exe gibt 0 für Erfolg (fehlerfrei) zurück.  Andernfalls der Linker die Fehlernummer, die den Link beendet.  Wenn der Linker LNK1104 generiert wird, gibt der Linker z. B. 1104 zurück.  Entsprechend ist die niedrigste Fehlernummer, die bei einem Fehler zurückgegeben, die vom Linker 1000.  Ein Rückgabewert von 128 stellt ein Konfigurationsproblem mit dem Betriebssystem oder einer .config-Datei dar; das Ladeprogramm link.exe oder c2.dll nicht geladen werden.

## <a name="see-also"></a>Siehe auch

[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)