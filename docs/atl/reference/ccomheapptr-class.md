---
title: CComHeapPtr-Klasse
ms.date: 11/04/2016
f1_keywords:
- CComHeapPtr
- ATLBASE/ATL::CComHeapPtr
- ATLBASE/ATL::CComHeapPtr::CComHeapPtr
helpviewer_keywords:
- CComHeapPtr class
ms.assetid: bd08b53d-da2b-43ab-a79c-e7c8dbbc5994
ms.openlocfilehash: eaa21700f63ae07565dba4b8b3b5dabac69e0168
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50553733"
---
# <a name="ccomheapptr-class"></a>CComHeapPtr-Klasse

Eine intelligente Zeiger-Klasse für die Verwaltung von Heap-Zeiger.

## <a name="syntax"></a>Syntax

```
template<typename T>
class CComHeapPtr : public CHeapPtr<T, CComAllocator>
```

#### <a name="parameters"></a>Parameter

*T*<br/>
Der Objekttyp, auf dem Heap gespeichert werden.

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

|Name|Beschreibung|
|----------|-----------------|
|[CComHeapPtr::CComHeapPtr](#ccomheapptr)|Der Konstruktor.|

## <a name="remarks"></a>Hinweise

`CComHeapPtr` leitet sich von `CHeapPtr`, verwendet jedoch [CComAllocator](../../atl/reference/ccomallocator-class.md) zur speicherbelegung mithilfe von COM-Routinen. Finden Sie unter [CHeapPtr](../../atl/reference/cheapptr-class.md) und [CHeapPtrBase](../../atl/reference/cheapptrbase-class.md) für die Methoden zur Verfügung.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CHeapPtrBase](../../atl/reference/cheapptrbase-class.md)

[CHeapPtr](../../atl/reference/cheapptr-class.md)

`CComHeapPtr`

## <a name="requirements"></a>Anforderungen

**Header:** atlbase.h

##  <a name="ccomheapptr"></a>  CComHeapPtr::CComHeapPtr

Der Konstruktor.

```
CComHeapPtr() throw();
explicit CComHeapPtr(T* pData) throw();
```

### <a name="parameters"></a>Parameter

*pData*<br/>
Ein vorhandenes `CComHeapPtr`-Objekt.

### <a name="remarks"></a>Hinweise

Der Heapzeiger kann optional erstellt werden unter Verwendung einer vorhandenen `CComHeapPtr` Objekt. Wenn dies der Fall ist, die neue `CComHeapPtr` Objekt übernimmt die Verantwortung für die Verwaltung der neue Zeiger und Ressourcen.

## <a name="see-also"></a>Siehe auch

[CHeapPtr-Klasse](../../atl/reference/cheapptr-class.md)<br/>
[CHeapPtrBase-Klasse](../../atl/reference/cheapptrbase-class.md)<br/>
[CComAllocator-Klasse](../../atl/reference/ccomallocator-class.md)<br/>
[Übersicht über die Klasse](../../atl/atl-class-overview.md)
