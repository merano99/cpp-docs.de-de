---
title: /DEFAULTLIB (Standardbibliothek festlegen)
ms.date: 05/29/2018
f1_keywords:
- VC.Project.VCLinkerTool.DefaultLibraries
- /defaultlib
helpviewer_keywords:
- -DEFAULTLIB linker option
- DEFAULTLIB linker option
- /DEFAULTLIB linker option
- libraries, adding to list of
ms.assetid: 6af7ff49-c170-4a13-97e2-2b9ae2de20c9
ms.openlocfilehash: 59a4b48e412cee6b2a90608747aa6fb3e1b79ca7
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326385"
---
# <a name="defaultlib-specify-default-library"></a>/DEFAULTLIB (Standardbibliothek festlegen)

Geben Sie eine Standardbibliothek zu suchen, um externe Verweise aufzulösen.

## <a name="syntax"></a>Syntax

> **/ DEFAULTLIB**:_Bibliothek_

### <a name="arguments"></a>Argumente

*Bibliothek*<br/>
Der Name einer Bibliothek beim Auflösen externer Verweise zu suchen.

## <a name="remarks"></a>Hinweise

Die **DEFAULTLIB** Option Fügt eine *Bibliothek* zur Liste der Bibliotheken, mit dem LINK gesucht werden, beim Auflösen von verweisen. Eine Bibliothek, die mit angegebenen **DEFAULTLIB** nach Bibliotheken, die explizit angegeben werden, in der Befehlszeile und vor dem Standardbibliotheken, die mit dem Namen OBJ-Dateien durchsucht.

Wenn Sie ohne Argumente wird die [/NODEFAULTLIB (Bibliotheken ignorieren)](../../build/reference/nodefaultlib-ignore-libraries.md) -Option überschreibt alle **DEFAULTLIB**:*Bibliothek* Optionen. Die **/NODEFAULTLIB**:*Bibliothek* überschreibt option **DEFAULTLIB**:*Bibliothek* wenn gleich *Bibliothek*Namen in beiden angegeben ist.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **Linker** > **Befehlszeile** Eigenschaftenseite.

1. In **zusätzliche Optionen**, geben Sie einen **DEFAULTLIB**:*Bibliothek* Option für jede Bibliothek suchen. Wählen Sie **OK** zum Speichern der Änderungen.

### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>Siehe auch

- [Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)
- [Linkeroptionen](../../build/reference/linker-options.md)
