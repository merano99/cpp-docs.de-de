---
title: 'Simpleactivationfactory:: Getruntimeclassname-Methode | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: module/Microsoft::WRL::SimpleActivationFactory::GetRuntimeClassName
dev_langs: C++
ms.assetid: 3aa07487-9a42-46f8-8893-37ba6315e50b
caps.latest.revision: "3"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 22cb09115938da3d90bbe7feac0aac490971ffd1
ms.sourcegitcommit: ca2f94dfd015e0098a6eaf5c793ec532f1c97de1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2017
---
# <a name="simpleactivationfactorygetruntimeclassname-method"></a>SimpleActivationFactory::GetRuntimeClassName-Methode

Ruft die Laufzeitklasse-Namen, der eine Instanz der Klasse, die gemäß der `Base` Klassenvorlagenparameter.

## <a name="syntax"></a>Syntax

```cpp
STDMETHOD( GetRuntimeClassName )(
    _Out_ HSTRING* runtimeName
);
```

### <a name="parameters"></a>Parameter

*runtimeName*  
Wenn dieser Vorgang abgeschlossen wird, der Name der Common Language Runtime-Klasse.

## <a name="return-value"></a>Rückgabewert

S_OK, wenn erfolgreich; andernfalls ein HRESULT, das den Fehler angibt.

## <a name="remarks"></a>Hinweise

Wenn &#95; &#95; WRL_STRICT &#95; &#95; wird definiert, ein Assert-Fehler wird ausgegeben, wenn die Klasse, wird angegeben die `Base` Klassenvorlagenparameter wird nicht von abgeleiteten [RuntimeClass](../windows/runtimeclass-class.md), oder ist nicht mit dem WinRt oder WinRtClassicComMix konfiguriert [ RuntimeClassType](../windows/runtimeclasstype-enumeration.md) -Enumerationswert.

## <a name="requirements"></a>Anforderungen

**Header:** module.h

**Namespace:** Microsoft::WRL

## <a name="see-also"></a>Siehe auch

[SimpleActivationFactory-Klasse](../windows/simpleactivationfactory-class.md)