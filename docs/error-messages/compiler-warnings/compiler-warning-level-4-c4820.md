---
title: "Compilerwarnung (Stufe 4) C4820 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4820"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4820"
ms.assetid: 17aa29f4-c287-49b8-bc43-8ed82ffed5ea
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Compilerwarnung (Stufe 4) C4820
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Bytes' Bytes Abstand nach dem Konstrukt 'member\_name'  
  
 Der Typ und die Anordnung von Elementen hat bewirkt, dass der Compiler nach einer Struktur Abstände eingefügt hat.  Weitere Informationen zum Hinzufügen von Abständen in einer Struktur finden Sie unter [align](../../cpp/align-cpp.md).  
  
 Diese Warnung ist standardmäßig deaktiviert.  Weitere Informationen finden Sie unter [Standardmäßig deaktivierte Compilerwarnungen](../../preprocessor/compiler-warnings-that-are-off-by-default.md).  
  
 Im folgenden Beispiel wird C4820 generiert:  
  
```  
// C4820.cpp  
// compile with: /W4 /c  
#pragma warning(default : 4820)   
  
// Delete the following 4 lines to resolve.  
__declspec(align(2)) struct MyStruct {  
   char a;  
   int i;   // C4820  
};  
  
// OK  
#pragma pack(1)  
__declspec(align(1)) struct MyStruct2 {  
   char a;  
   int i;  
};  
```