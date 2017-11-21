---
title: Compiler-Fehler C2749 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2749
dev_langs: C++
helpviewer_keywords: C2749
ms.assetid: a81aef36-cdca-4d78-89d5-b72eff2500b2
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 23eb174bd161f14351fae18ae4aba72f427da4ed
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2749"></a>Compiler-Fehler C2749 generiert
'Typ': kann nur ausgelöst oder abgefangen Handle für eine verwaltete Klasse mit/clr: safe  
  
 Bei Verwendung **/CLR: safe**, kann nur ausgelöst oder abgefangen einen Referenztyp darstellt.  
  
 Weitere Informationen finden Sie unter [/clr (Common Language Runtime-Kompilierung)](../../build/reference/clr-common-language-runtime-compilation.md).  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2749 generiert:  
  
```  
// C2749.cpp  
// compile with: /clr:safe  
ref struct MyStruct {  
public:  
   int i;  
};  
  
int main() {  
   MyStruct ^x = gcnew MyStruct;  
  
   // Delete the following 4 lines to resolve.  
   try {   
      throw (1);   // C2749  
   }  
   catch(int){}  
  
   // OK  
   try {  
      throw (x);  
   }  
   catch(MyStruct ^){}   
}  
```