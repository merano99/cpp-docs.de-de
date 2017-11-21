---
title: . LIB-Dateien als Linkereingabe | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: VC.Project.VCLinkerTool.AdditionalDependencies
dev_langs: C++
helpviewer_keywords:
- OMF libraries
- linking [C++], OMF libraries
- import libraries, linker files
- libraries [C++], .lib files as linker input
- COFF files, import libraries
- default libraries [C++], linker output
- default libraries [C++]
- defaults [C++], libraries
- .lib files
ms.assetid: dc5d2b1c-2487-41fa-aa71-ad1e0647958b
caps.latest.revision: "15"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: ad61a8fa3672dd6f243c611e8ad363769dc5fa05
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="lib-files-as-linker-input"></a>.LIB-Dateien als Linkereingabe
LINK akzeptiert COFF-Standardbibliotheken und COFF-Bibliotheken, die in der Regel die Erweiterung haben. Lib. Standardbibliotheken Objekte enthalten und werden durch die LIB-Tool erstellt. Importbibliotheken enthalten Informationen über Exporte in andere Programme, und es werden entweder durch LINK erstellt, wenn sie ein Programm erstellt, das Exporte enthält, oder durch die LIB-Tool. Informationen zur Verwendung von LIB standard erstellen oder importieren Bibliotheken finden Sie unter [LIB-Referenz](../../build/reference/lib-reference.md). Weitere Informationen zur Verwendung von LINK eine Importbibliothek zu erstellen, finden Sie unter der [/DLL](../../build/reference/dll-build-a-dll.md) Option.  
  
Eine Bibliothek wird als ein Dateiname als Argument oder eine Standardbibliothek zu verknüpfen angegeben. LINK Auflösen externer Verweise durch suchen zuerst in Bibliotheken, die in der Befehlszeile angegeben, und klicken Sie dann im Standardmodus Bibliotheken angegeben, mit der [Option](../../build/reference/defaultlib-specify-default-library.md) Option, und klicken Sie dann im Standardmodus Bibliotheken mit dem Namen in der OBJ-Dateien. Wenn ein Pfad mit der Bibliotheksname angegeben ist, sucht LINK für die Bibliothek in diesem Verzeichnis. Wenn kein Pfad angegeben wird, sucht LINK zuerst in das Verzeichnis, dem von LINK ausgeführt wird, und klicken Sie dann in den Verzeichnissen, die in der LIB-Umgebungsvariablen angegeben.  
  
## <a name="to-add-lib-files-as-linker-input-in-the-development-environment"></a>LIB-Dateien als Linkereingabe in der Entwicklungsumgebung hinzufügen  
  
1.  Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [arbeiten mit Projekteigenschaften](../../ide/working-with-project-properties.md).  
  
2.  Wählen Sie die **Eingabe** Eigenschaftenseite in der **Linker** Ordner.  
  
3.  Ändern der **zusätzliche Abhängigkeiten** Eigenschaft, die LIB-Dateien hinzuzufügen.  
  
## <a name="to-programmatically-add-lib-files-as-linker-input"></a>So fügen Sie programmgesteuert LIB-Dateien als Linkereingabe hinzu  
  
-   Finden Sie unter [AdditionalDependencies](https://msdn.microsoft.com/library/microsoft.visualstudio.vcprojectengine.vclinkertool.additionaldependencies.aspx).  
  
## <a name="example"></a>Beispiel  
Im folgende Beispiel veranschaulicht das Erstellen und Verwenden einer LIB-Datei. Erstellen Sie zuerst eine LIB-Datei ein:  
  
```cpp  
// lib_link_input_1.cpp  
// compile by using: cl /LD lib_link_input_1.cpp  
__declspec(dllexport) int Test() {  
   return 213;  
}  
```  
  
Und kompilieren Sie dieses Beispiel mithilfe der LIB-Datei, die Sie soeben erstellt haben:  
  
```cpp  
// lib_link_input_2.cpp  
// compile by using: cl /EHsc lib_link_input_1.lib lib_link_input_2.cpp   
__declspec(dllimport) int Test();  
#include <iostream>  
int main() {  
   std::cout << Test() << std::endl;  
}  
```  
  
```Output  
213  
```  
  
## <a name="see-also"></a>Siehe auch  
 [LINK-Eingabedateien](../../build/reference/link-input-files.md)   
 [Linkeroptionen](../../build/reference/linker-options.md)