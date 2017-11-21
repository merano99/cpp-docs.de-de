---
title: 'Makeallocator:: Detach-Methode | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: implements/Microsoft::WRL::Details::MakeAllocator::Detach
dev_langs: C++
helpviewer_keywords: Detach method
ms.assetid: 78012634-2dda-4ea2-9ffe-40f105d2fe47
caps.latest.revision: "5"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 2dabfbbc205e340b74498f422e2802f481c23275
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="makeallocatordetach-method"></a>MakeAllocator::Detach-Methode
Unterstützt die WRL-Infrastruktur und ist nicht direkt aus Ihrem Code verwendet werden soll.  
  
## <a name="syntax"></a>Syntax  
  
```  
__forceinline void Detach();  
```  
  
## <a name="remarks"></a>Hinweise  
 Hebt die Zuordnung von belegten Arbeitsspeicher die [Allocate](../windows/makeallocator-allocate-method.md) Methode aus dem aktuellen MakeAllocator-Objekt.  
  
 Wenn Sie Detach() aufrufen, sind Sie verantwortlich für das Löschen des Arbeitsspeichers, die von der Allocate-Methode bereitgestellt.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## <a name="see-also"></a>Siehe auch  
 [MakeAllocator-Klasse](../windows/makeallocator-class.md)   
 [Microsoft::WRL::Details-Namespace](../windows/microsoft-wrl-details-namespace.md)