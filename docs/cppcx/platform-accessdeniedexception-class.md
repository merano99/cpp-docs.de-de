---
title: Platform::AccessDeniedException-Klasse
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::AccessDeniedException
- VCCORLIB/Platform::AccessDeniedException::AccessDeniedException
helpviewer_keywords:
- Platform::AccessDeniedException
ms.assetid: 6ae2155b-7b16-4587-8d2d-da05eab4c7e9
ms.openlocfilehash: 4865492e3b5d8e4acc35e58081a226c9e66ed99f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50588148"
---
# <a name="platformaccessdeniedexception-class"></a>Platform::AccessDeniedException-Klasse

Wird ausgelöst, wenn der Zugriff auf eine Ressource oder eine Funktion verweigert wird.

## <a name="syntax"></a>Syntax

```cpp
public ref class AccessDeniedException : COMException,    IException,    IPrintable,   IEquatable
```

### <a name="remarks"></a>Hinweise

Wenn Sie diese Ausnahme erreicht haben, stellen Sie sicher, dass Sie die entsprechende Funktion angefordert und die erforderlichen Deklarationen im Paketmanifest der App angegeben haben. Weitere Informationen finden Sie unter [COMException](../cppcx/platform-comexception-class.md) .

### <a name="requirements"></a>Anforderungen

**Unterstützter Client (Min.):** Windows 8

**Unterstützter Server (Min.):** Windows Server 2012

**Namespace:** Platform

**Metadaten:** platform.winmd

## <a name="see-also"></a>Siehe auch

[Platform::COMException-Klasse](../cppcx/platform-comexception-class.md)