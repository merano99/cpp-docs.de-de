---
title: Platform::Metadata::DefaultMemberAttribute-Attribut
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Metadata::DefaultMemberAttribute
helpviewer_keywords:
- Platform::Metadata::DefaultMemberAttribute Attribute
ms.assetid: d8abda01-c257-4371-aec4-541d4825e0af
ms.openlocfilehash: a4b3d5e8ab5d6ce254560bc84daceac74e2c9ca1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50486657"
---
# <a name="platformmetadatadefaultmemberattribute-attribute"></a>Platform::Metadata::DefaultMemberAttribute-Attribut

Gibt die bevorzugte Funktion an, um unter mehreren möglichen überladenen Funktionen aufzurufen.

## <a name="syntax"></a>Syntax

```cpp
public ref class DefaultMember abstract : Attribute
```

## <a name="inheritance"></a>Vererbung

[Platform::Object](../cppcx/platform-object-class.md)

[Platform::Metadata::Attribute](../cppcx/platform-metadata-attribute-attribute.md)

### <a name="remarks"></a>Hinweise

Wenden Sie das DefaultMember-Attribut auf eine Methode an, die von einer JavaScript-Anwendung verwendet wird.

### <a name="requirements"></a>Anforderungen

**Unterstützter Client (Min.):** Windows 8

**Unterstützter Server (Min.):** Windows Server 2012

**Namespace:** Platform::Metadata

**Metadaten:** platform.winmd

## <a name="see-also"></a>Siehe auch

[Platform::Metadata-Namespace](../cppcx/platform-metadata-namespace.md)