---
title: /Gw (Optimieren globaler Daten)
ms.date: 11/04/2016
f1_keywords:
- /Gw
helpviewer_keywords:
- /Gw compiler option [C++]
- -Gw compiler option [C++]
ms.assetid: 6f90f4e9-5eb8-4c47-886e-631278a5a4a9
ms.openlocfilehash: 406b1577b77f056e18753db10bae5675febe879e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50506690"
---
# <a name="gw-optimize-global-data"></a>/Gw (Optimieren globaler Daten)

Fasst globale Daten zur Optimierung in COMDAT-Abschnitten zusammen.

## <a name="syntax"></a>Syntax

```
/Gw[-]
```

## <a name="remarks"></a>Hinweise

Die **"/ GW"** Option bewirkt, dass den Compiler globale Daten in einzelnen COMDAT-Abschnitten. In der Standardeinstellung **"/ GW"** ist deaktiviert und muss explizit aktiviert werden kann. Verwenden Sie zur expliziten Deaktivierung, **/Gw-**. Wenn beide **"/ GW"** und ["/ GL"](../../build/reference/gl-whole-program-optimization.md) sind aktiviert, verwendet der Linker Optimierung des ganzen Programms um COMDAT-Abschnitten über mehrere Objektdateien hinweg zu vergleichen, um nicht referenzierte globale Daten ausgeschlossen oder zum Zusammenführen Identische schreibgeschützte globale Daten. Dies kann die Größe der resultierenden binären ausführbaren Datei deutlich reduzieren.

Wenn Sie separat kompilieren und verknüpfen, können Sie mithilfe der [/OPT: REF](../../build/reference/opt-optimizations.md) Linkeroption, um die ausführbare Datei ausgeschlossen, die nicht referenzierten globalen Daten in Objektdateien, kompiliert mit, der **"/ GW"** Option.

Sie können auch die [/OPT: ICF](../../build/reference/opt-optimizations.md) und ["/ LTCG"](../../build/reference/ltcg-link-time-code-generation.md) Optionen des Linkers zusammen, um in der ausführbaren Datei zusammenführen alle identischen schreibgeschützte globalen Daten über mehrere Objektdateien hinweg mit kompiliert die **"/ GW"** Option.

Weitere Informationen finden Sie unter [Einführung in "/ GW" Compilerschalter](http://blogs.msdn.com/b/vcblog/archive/2013/09/11/introducing-gw-compiler-switch.aspx) im Visual C++-Teamblog.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Ausführliche Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **C/C++-** Ordner.

1. Wählen Sie die **Befehlszeile** Eigenschaftenseite.

1. Ändern der **zusätzliche Optionen** Eigenschaft sollen **"/ GW"** und wählen Sie dann **OK**.

### <a name="to-set-this-compiler-option-programmatically"></a>So legen Sie diese Compileroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>Siehe auch

[Compileroptionen](../../build/reference/compiler-options.md)<br/>
[Festlegen von Compileroptionen](../../build/reference/setting-compiler-options.md)