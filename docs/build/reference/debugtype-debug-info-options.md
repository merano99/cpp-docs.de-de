---
title: / DEBUGTYPE (Debuginformationsoptionen)
ms.date: 11/04/2016
f1_keywords:
- /debugtype
helpviewer_keywords:
- /DEBUGTYPE linker option
- DEBUGTYPE linker option
- -DEBUGTYPE linker option
ms.assetid: 1ddcb718-7fec-4f92-a319-3f70f04fe742
ms.openlocfilehash: f730e485b7dc29cb8fe98bdcc7ea50f5e8c622d7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50676992"
---
# <a name="debugtype-debug-info-options"></a>/ DEBUGTYPE (Debuginformationsoptionen)

Die Option „/DEBUGTYPE“ gibt die Typen der durch die Option „/DEBUG“ generierten Debuginformationen an.

```
/DEBUGTYPE:[CV | PDATA | FIXUP]
```

## <a name="arguments"></a>Argumente

**KREUZVALIDIERUNG**<br/>
Weist den Linker an, Debuginformationen für Symbole, Zeilennummern und andere Objektkompilierungsinformationen in der PDB-Datei auszugeben. Diese Option ist standardmäßig aktiviert Wenn **/DEBUG** angegeben ist und **/DEBUGTYPE** nicht angegeben ist.

**PDATA**<br/>
Weist den Linker an, den Debugstreaminformationen in der PDB-Datei PDATA- und XDATA-Einträge hinzuzufügen. Diese Option ist standardmäßig aktiviert Wenn sowohl die **/DEBUG** und **/Driver** Optionen angegeben werden. Wenn **/DEBUGTYPE:PDATA** wird angegeben, der Linker automatisch die Debugsymbole in die PDB-Datei. Wenn **/DEBUGTYPE:PDATA, FIXUP** angegeben ist, wird der Linker enthält keine Debugsymbole in die PDB-Datei.

**FIXUP**<br/>
Weist den Linker an, den Debugstreaminformationen in der PDB-Datei Umsetzungstabelleneinträge hinzuzufügen. Diese Option ist standardmäßig aktiviert Wenn sowohl die **/DEBUG** und **/PROFILE** Optionen angegeben werden. Wenn **/DEBUGTYPE:FIXUP** oder **/DEBUGTYPE:FIXUP, PDATA** angegeben ist, wird der Linker enthält keine Debugsymbole in die PDB-Datei.

Argumente für **/DEBUGTYPE** kann in einer beliebigen Reihenfolge kombiniert werden, indem Sie sie durch ein Komma trennen. Die **/DEBUGTYPE** Option und ihrer Argumente wird keine Groß-/Kleinschreibung beachtet.

## <a name="remarks"></a>Hinweise

Verwenden der **/DEBUGTYPE** Option aus, um die Einbindung der Verschiebung-Tabelle-Daten oder der pdata- und XData-Headerinformationen im Debugstream anzugeben. Dadurch schließt der Linker Informationen über Benutzermoduscode mit ein, der in einem Kerneldebugger sichtbar ist, wenn die Aufschlüsselung in einen Kernelmoduscode erfolgt. Wenn Debugsymbole zur Verfügung stellen **FIXUP** wird angegeben, umfassen die **CV** Argument.

So debuggen Sie Code im Benutzermodus, der für Anwendungen typisch ist, die **/DEBUGTYPE** Option ist nicht erforderlich. In der Standardeinstellung die Compilerschaltern, die angeben, Debuggen von Ausgabe ([/Z7, / Zi, / Zi](../../build/reference/z7-zi-zi-debug-information-format.md)) alle die Informationen vom Visual Studio debugger benötigt-ausgeben. Verwendung **/DEBUGTYPE:PDATA** oder **/DEBUGTYPE:CV, PDATA, FIXUP** , Code zu debuggen, der Benutzermodus- und Kernelmodus-Komponenten, z. B. eine Konfigurations-app für einen Gerätetreiber kombiniert. Weitere Informationen über kernelmodusdebugger finden Sie unter [Debugging-Tools für Windows (WinDbg, KD, CDB, NTSD)](/windows-hardware/drivers/debugger/index)

## <a name="see-also"></a>Siehe auch

[/DEBUG (Debuginfo generieren)](../../build/reference/debug-generate-debug-info.md)<br/>
[/DRIVER (Windows NT-Kernelmodustreiber)](../../build/reference/driver-windows-nt-kernel-mode-driver.md)<br/>
[/PROFILE (Leistungstoolprofiler)](../../build/reference/profile-performance-tools-profiler.md)<br/>
[Debugtools für Windows (WinDbg, KD, CDB, NTSD)](/windows-hardware/drivers/debugger/index)