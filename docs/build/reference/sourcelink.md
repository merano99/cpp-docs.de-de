---
title: / SOURCELINK (umfassen Sourcelink-Datei in die PDB-Datei)
ms.date: 08/20/2018
f1_keywords:
- /sourcelink
helpviewer_keywords:
- /SOURCELINK linker option
- /SOURCELINK
ms.openlocfilehash: a5a01ca56a49791a608c5c836312c7728e9328c3
ms.sourcegitcommit: fe1e21df175cd004d21c6e4659082efceb649a8b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/02/2019
ms.locfileid: "53978282"
---
# <a name="sourcelink-include-source-link-file-in-pdb"></a>/ SOURCELINK (umfassen Link "Quelle"-Datei in die PDB-Datei)

Gibt eine Link "Quelle"-Konfigurationsdatei in der vom Linker generierte PDB-Datei eingeschlossen werden sollen.

## <a name="syntax"></a>Syntax

> **/ SOURCELINK:**_Dateiname_

## <a name="arguments"></a>Argumente

*filename*<br/>
Gibt eine JSON-formatierte Konfigurationsdatei, die eine einfache Zuordnung der lokalen Dateipfade, URLs enthält, in dem die Quelldatei abgerufen werden kann, für die Anzeige durch den Debugger. Weitere Informationen zum Format dieser Datei finden Sie unter [JSON-Schema der Datenquellensicht-Link](https://github.com/dotnet/designs/blob/master/accepted/diagnostics/source-link.md#source-link-json-schema).

## <a name="remarks"></a>Hinweise

Link "Quelle" ist eine Sprache – und unabhängig Quellcodeverwaltungssystem für die Bereitstellung von Quelle für Binärdateien zu debuggen. Link "Quelle" wird für systemeigene C++-Binärdateien, die in Visual Studio 2017 Version 15.8 ab unterstützt. Eine Übersicht der Link "Quelle", finden Sie unter [Link "Quelle"](https://github.com/dotnet/designs/blob/master/accepted/diagnostics/source-link.md). Informationen zum Link "Quelle" in Ihren Projekten zu verwenden und wie Sie die SourceLink-Datei als Teil Ihres Projekts zu generieren, finden Sie unter [mithilfe des Quelllinks](https://github.com/dotnet/sourcelink#using-source-link-in-c-projects).

### <a name="to-set-the-sourcelink-linker-option-in-visual-studio"></a>So legen Sie die /SOURCELINK-Linkeroption in Visual Studio fest

1. Öffnen der **Eigenschaftenseiten** im Dialogfeld für das Projekt. Weitere Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **Linker** > **Befehlszeile** Eigenschaftenseite.

1. In der **zusätzliche Optionen** fügen **/SOURCELINK:**_Filename_ und wählen Sie dann **OK** oder **übernehmen**zum Speichern der Änderungen.

### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest

- Diese Option ist keine programmgesteuerte Variante verfügbar sein.

## <a name="see-also"></a>Siehe auch

[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)
