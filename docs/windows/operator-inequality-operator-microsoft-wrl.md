---
title: 'Operator! =-Operator (Microsoft:: wrl) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: client/Microsoft::WRL::operator!=
dev_langs: C++
ms.assetid: 785435da-87a6-4454-9bce-9d288a96dc26
caps.latest.revision: "3"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 7c4219cc4bd7a4445a483c9af816e43b6485bbdd
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="operator-operator-microsoftwrl"></a>operator!=-Operator (Microsoft::WRL)
Ungleichheitsoperator für [ComPtr](../windows/comptr-class.md) und [ComPtrRef](../windows/comptrref-class.md) Objekte.  
  
## <a name="syntax"></a>Syntax  
  
```  
WRL_NOTHROW bool operator!=(  
   const ComPtr<T>& a,  
   const ComPtr<U>& b  
);  
WRL_NOTHROW bool operator!=(  
   const ComPtr<T>& a,  
   decltype(__nullptr)  
);  
WRL_NOTHROW bool operator!=(  
   decltype(__nullptr),  
   const ComPtr<T>& a  
);  
WRL_NOTHROW bool operator!=(  
   const Details::ComPtrRef<ComPtr<T>>& a,  
   const Details::ComPtrRef<ComPtr<U>>& b  
);  
WRL_NOTHROW bool operator!=(  
   const Details::ComPtrRef<ComPtr<T>>& a,  
   decltype(__nullptr)  
);  
WRL_NOTHROW bool operator!=(  
   decltype(__nullptr),  
   const Details::ComPtrRef<ComPtr<T>>& a  
);  
WRL_NOTHROW bool operator!=(  
   const Details::ComPtrRef<ComPtr<T>>& a,  
   void* b  
);  
WRL_NOTHROW bool operator!=(  
   void* b,  
   const Details::ComPtrRef<ComPtr<T>>& a  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `a`  
 Das linke Objekt.  
  
 `b`  
 Das rechte Objekt.  
  
## <a name="return-value"></a>Rückgabewert  
 `true`Wenn die Objekte nicht gleich sind; andernfalls `false`.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## <a name="see-also"></a>Siehe auch  
 [Microsoft::WRL-Namespace](../windows/microsoft-wrl-namespace.md)