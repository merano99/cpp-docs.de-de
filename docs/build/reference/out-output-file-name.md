---
title: /OUT (Ausgabedateiname)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.OutputFile
- /out
helpviewer_keywords:
- output files, name linker option
- -OUT linker option
- OUT linker option
- /OUT C++ linker option
- linker [C++], output files
ms.assetid: 976210a4-e51f-4cfb-af5e-c16344455834
ms.openlocfilehash: f5ba323b830b9d06956d88d957206e3f73c15418
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50497178"
---
# <a name="out-output-file-name"></a>/OUT (Ausgabedateiname)

```
/OUT:filename
```

## <a name="arguments"></a>Argumente

*filename*<br/>
Ein vom Benutzer angegebene Name für die Ausgabedatei. Sie können den Standardnamen ersetzt.

## <a name="remarks"></a>Hinweise

Die Option/Out überschreibt den Standardnamen und den Speicherort des Programms, das der Linker erstellt.

In der Standardeinstellung bildet der Linker den Dateinamen mithilfe der Basisname der zuerst angegebenen OBJ-Datei und der geeigneten Erweiterung (.exe oder .dll).

Standardbasisname für eine Bibliothek Standardbasisname oder importieren Sie diese option. Weitere Informationen finden Sie unter [Zuordnungsdatei generieren](../../build/reference/map-generate-mapfile.md) (/ MAP) und [/IMPLIB](../../build/reference/implib-name-import-library.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [Einstellung von Visual C++-Projekteigenschaften](../../ide/working-with-project-properties.md).

1. Klicken Sie auf die **Linker** Ordner.

1. Klicken Sie auf die **allgemeine** Eigenschaftenseite.

1. Ändern der **Ausgabedatei** Eigenschaft.

### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.OutputFile%2A>.

## <a name="see-also"></a>Siehe auch

[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)