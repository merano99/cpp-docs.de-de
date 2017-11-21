---
title: -DEF (Moduldefinitionsdatei festlegen) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VC.Project.VCLinkerTool.ModuleDefinitionFile
- /def
dev_langs: C++
helpviewer_keywords:
- module definition files, specifying
- DEF linker option
- -DEF linker option
- module definition files
- /DEF linker option
ms.assetid: 6497fa68-65f0-48ca-8f66-b87166fc631a
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 3ed21549aace74bab5944236bdb26e409a287155
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="def-specify-module-definition-file"></a>/DEF (Moduldefinitionsdatei festlegen)
```  
/DEF:filename  
```  
  
## <a name="remarks"></a>Hinweise  
 Dabei gilt:  
  
 *filename*  
 Der Name der Moduldefinitionsdatei (.def) an den Linker übergeben werden.  
  
## <a name="remarks"></a>Hinweise  
 Die Option/DEF übergibt eine Moduldefinitionsdatei (.def) an den Linker. Link kann nur eine DEF-Datei angegeben werden. Einzelheiten zu DEF-Dateien finden Sie unter [Moduldefinitionsdateien](../../build/reference/module-definition-dot-def-files.md).  
  
### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest  
  
1.  Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [Einstellung von Visual C++-Projekteigenschaften](../../ide/working-with-project-properties.md).  
  
2.  Klicken Sie auf die **Linker** Ordner.  
  
3.  Klicken Sie auf die **Eingabe** Eigenschaftenseite.  
  
4.  Ändern der **Moduldefinitionsdatei** Eigenschaft.  
  
 Um eine DEF-Datei in der Entwicklungsumgebung anzugeben, sollten Sie es dem Projekt zusammen mit anderen Dateien hinzufügen und geben dann die Datei an die DEF-Option.  
  
### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest  
  
-   Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ModuleDefinitionFile%2A>.  
  
## <a name="see-also"></a>Siehe auch  
 [Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)   
 [Linkeroptionen](../../build/reference/linker-options.md)