---
title: "Compilerwarnung (Stufe 4) C4212 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4212"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4212"
ms.assetid: df781ea1-182d-4f9f-9a31-55b6ce80c711
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerwarnung (Stufe 4) C4212
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Nicht dem Standard entsprechende Erweiterung: Funktionsdeklaration verwendet Ellipse \(...\)  
  
 Der Funktionsprototyp hat eine variable Anzahl von Argumenten.  Dies trifft auf die Funktionsdefinition nicht zu.  
  
 Im folgenden Beispiel wird C4212 generiert:  
  
```  
// C4212.c  
// compile with: /W4 /Ze /c  
void f(int , ...);  
void f(int i, int j) {}  
```