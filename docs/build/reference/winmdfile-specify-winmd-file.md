---
title: /WINMDFILE (winmd-Datei angeben)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.GenerateWindowsMetadataFile
ms.assetid: 062b41b3-14d6-432c-a361-fdb66e918931
ms.openlocfilehash: 74958e51925b9ed6d1382efe76fe587eed73f4e7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50656053"
---
# <a name="winmdfile-specify-winmd-file"></a>/WINMDFILE (winmd-Datei angeben)

Gibt den Dateinamen für die Windows-Runtime-Metadatendatei (.winmd)-Ausgabedatei, die vom generierten der [/WINMD](../../build/reference/winmd-generate-windows-metadata.md) -Linkeroption.

```
/WINMDFILE:filename
```

## <a name="remarks"></a>Hinweise

Verwenden Sie den Wert, der im angegebenen `filename` zum Überschreiben des Standardnamens winmd-Datei (`binaryname`.winmd). Beachten Sie, dass Sie keine ".winmd" zum Anfügen `filename`.  Wenn mehrere Werte aufgeführt sind, auf die **/winmdfile** über die Befehlszeile, die letzte Vorrang.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Ausführliche Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Linker** Ordner.

1. Wählen Sie die **Windows-Metadaten** Eigenschaftenseite.

1. In der **Windows-Metadatendatei** Geben Sie den Dateispeicherort.

## <a name="see-also"></a>Siehe auch

[/WINMD (Windows-Metadaten generieren)](../../build/reference/winmd-generate-windows-metadata.md)<br/>
[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)