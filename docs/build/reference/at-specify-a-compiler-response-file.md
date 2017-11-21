---
title: '@ (Compiler-Antwortdateien festlegen) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: '@'
dev_langs: C++
helpviewer_keywords:
- response files, C/C++ compiler
- '@ compiler option'
- cl.exe compiler, specifying response files
ms.assetid: 400fffee-909d-4f60-bf76-45833e822685
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: fcbadb55b2116b0939bbb954e4f544c40caacebb
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="-specify-a-compiler-response-file"></a>@ (Compiler-Antwortdateien festlegen)
Gibt eine Compiler-Antwortdateien an.  
  
## <a name="syntax"></a>Syntax  
  
```  
@response_file  
```  
  
## <a name="arguments"></a>Argumente  
 `response_file`  
 Eine Textdatei, die Compilerbefehle enthält.  
  
## <a name="remarks"></a>Hinweise  
 Eine Antwortdatei darf keine Befehle, die Sie in der Befehlszeile angeben möchten. Dies kann hilfreich, wenn die Befehlszeilenargumente 127 Zeichen lang sein.  
  
 Es ist nicht möglich, geben Sie die  **@**  -Option innerhalb einer Antwortdatei. Eine Antwortdatei kann nicht, also eine andere Antwortdatei einbetten.  
  
 Über die Befehlszeile können Sie beliebig viele Antwortdateioptionen angeben (z. B. `@respfile.1 @respfile.2`) wie gewünscht.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest  
  
-   Eine Antwortdatei kann nicht in der Entwicklungsumgebung angegeben werden und muss in der Befehlszeile angegeben werden.  
  
### <a name="to-set-this-compiler-option-programmatically"></a>So legen Sie diese Compileroption programmgesteuert fest  
  
-   Diese Compileroption kann programmgesteuert geändert werden.  
  
## <a name="see-also"></a>Siehe auch  
 [Compileroptionen](../../build/reference/compiler-options.md)   
 [Festlegen von Compileroptionen](../../build/reference/setting-compiler-options.md)