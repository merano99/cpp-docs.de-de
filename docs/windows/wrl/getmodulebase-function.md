---
title: GetModuleBase-Funktion
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::GetModuleBase
ms.assetid: 123d3b14-2eaf-4e02-8dcd-b6567917c6a6
ms.openlocfilehash: 4d8c8467b7aeb9c21bf5f4ee19c60e6e60880688
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336105"
---
# <a name="getmodulebase-function"></a>GetModuleBase-Funktion

Ruft eine [ModuleBase](modulebase-class.md) Zeiger, der inkrementiert und dekrementiert den Verweiszähler des ermöglicht eine [RuntimeClass](runtimeclass-class.md) Objekt.

## <a name="syntax"></a>Syntax

```cpp
inline Details::ModuleBase* GetModuleBase() throw()
```

## <a name="return-value"></a>Rückgabewert

Ein Zeiger auf ein `ModuleBase` -Objekt.

## <a name="remarks"></a>Hinweise

Diese Funktion wird intern zum Inkrementieren und Dekrementieren verwendet Verweiszähler des Objekts.

Sie können diese Funktion verwenden, zum Steuern der Verweiszähler durch Aufrufen von [modulebase:: Incrementobjectcount](modulebase-class.md#incrementobjectcount) und [modulebase:: Decrementobjectcount](modulebase-class.md#decrementobjectcount).

## <a name="requirements"></a>Anforderungen

**Header:** implements.h

**Namespace:** Microsoft::WRL

## <a name="see-also"></a>Siehe auch

[Microsoft::WRL-Namespace](microsoft-wrl-namespace.md)