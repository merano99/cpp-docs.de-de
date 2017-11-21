---
title: Kopieren (STL/CLR) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::copy
dev_langs: C++
helpviewer_keywords: copy function [STL/CLR]
ms.assetid: f6738535-fde6-446e-a797-bf2b457c2bff
caps.latest.revision: "4"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 525d7c0499c0cdacfdc7b2b12b64d8d099de3197
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="copy-stlclr"></a>copy (STL/CLR)
Weist die Werte von Elementen aus einem Quellbereich einem Zielbereich zu, durchläuft die Quellelementsequenz und weist ihnen vorwärts neue Positionen zu.  
  
## <a name="syntax"></a>Syntax  
  
```  
template<class _InIt, class _OutIt> inline  
    _OutIt copy(_InIt _First, _InIt _Last, _OutIt _Dest);  
```  
  
## <a name="remarks"></a>Hinweise  
 Diese Funktion verhält sich wie die C++-Standardbibliothek Funktion `copy`. Weitere Informationen finden Sie unter [Kopie](http://msdn.microsoft.com/Library/f1fec7da-e01b-40f1-b5bd-6b81e304cae1).  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext-Algorithmus >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [algorithm (STL/CLR)](../dotnet/algorithm-stl-clr.md)