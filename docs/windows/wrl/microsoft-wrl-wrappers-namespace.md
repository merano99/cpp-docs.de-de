---
title: Microsoft::WRL::Wrappers-Namespace
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers
helpviewer_keywords:
- Wrappers namespace
ms.assetid: 36ac38c7-1fc3-42da-a879-5c68661dc9e1
ms.openlocfilehash: 953318e09c4c0d00748f2b6189615dbd66677a96
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54335989"
---
# <a name="microsoftwrlwrappers-namespace"></a>Microsoft::WRL::Wrappers-Namespace

Definiert die Resource Acquisition ist Initialisierung (RAII) Wrappertypen, die die Verwaltung der Lebensdauer von Objekten, Zeichenfolgen und Handles zu vereinfachen.

## <a name="syntax"></a>Syntax

```cpp
namespace Microsoft::WRL::Wrappers;
```

## <a name="members"></a>Member

### <a name="typedefs"></a>Typedefs

|Name|Beschreibung|
|----------|-----------------|
|`FileHandle`|`HandleT<HandleTraits::FileHandleTraits>`|

### <a name="classes"></a>Klassen

|Name|Beschreibung|
|----------|-----------------|
|[CriticalSection-Klasse](criticalsection-class.md)|Stellt ein kritisches Abschnittsobjekt dar.|
|[Ereignisklasse (WRL)](event-class-wrl.md)|Stellt ein Ereignis dar.|
|[HandleT-Klasse](handlet-class.md)|Stellt ein Handle für ein Objekt dar.|
|[HString-Klasse](hstring-class.md)|Bietet Unterstützung für die Bearbeitung von HSTRING-Handles.|
|[HStringReference-Klasse](hstringreference-class.md)|Stellt ein HSTRING dar, das aus einer vorhandenen Zeichenfolge erstellt wird.|
|[Mutex-Klasse](mutex-class.md)|Stellt ein Synchronisierungsobjekt, das ausschließlich auf eine freigegebene Ressource steuert.|
|[RoInitializeWrapper-Klasse](roinitializewrapper-class.md)|Initialisiert die Windows-Runtime.|
|[Semaphore-Klasse](semaphore-class.md)|Stellt ein Synchronisierungsobjekt, das eine freigegebene Ressource steuert, die eine begrenzte Anzahl von Benutzern unterstützen können.|
|[SRWLock-Klasse](srwlock-class.md)|Stellt eine slim Reader-/Writer-Sperre.|

## <a name="requirements"></a>Anforderungen

**Header:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>Siehe auch

[Microsoft::WRL-Namespace](microsoft-wrl-namespace.md)