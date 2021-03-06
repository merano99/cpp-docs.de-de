---
title: /NOENTRY (Kein Einstiegspunkt)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.ResourceOnlyDLL
- /noentry
helpviewer_keywords:
- entry points [C++], linker specifying
- -NOENTRY linker option
- resource-only DLLs [C++], creating
- NOENTRY linker option
- /NOENTRY linker option [C++]
- DLLs [C++], creating
ms.assetid: 0214dd41-35ad-43ab-b892-e636e038621a
ms.openlocfilehash: fef4340fa4bb130ac54f4d5e66d4cd4d2f2a3049
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50607362"
---
# <a name="noentry-no-entry-point"></a>/NOENTRY (Kein Einstiegspunkt)

```
/NOENTRY
```

## <a name="remarks"></a>Hinweise

Die Option/NOENTRY ist erforderlich für das Erstellen einer reinen Ressourcen-DLL, die keinen ausführbaren Code enthält. Weitere Informationen finden Sie unter [Erstellen einer DLL Resource-Only](../../build/creating-a-resource-only-dll.md).

Sie können mit dieser Option verhindern, dass LINK einen Verweis auf `_main` in die DLL einbindet.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [Einstellung von Visual C++-Projekteigenschaften](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Linker** Ordner.

1. Wählen Sie die **erweitert** Eigenschaftenseite.

1. Ändern der **kein Einstiegspunkt** Eigenschaft.

### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest

1. Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ResourceOnlyDLL%2A>.

## <a name="see-also"></a>Siehe auch

[Erstellen einer DLL als reine Ressource](../../build/creating-a-resource-only-dll.md)<br/>
[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)