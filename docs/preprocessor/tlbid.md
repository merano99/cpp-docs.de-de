---
title: tlbid
ms.date: 10/18/2018
f1_keywords:
- tlbid
helpviewer_keywords:
- tlbid attribute
ms.assetid: 54b06785-191b-4e77-a9a5-485f2b4acb09
ms.openlocfilehash: 31b71f7c195a7e2ee649b40197551e4ff5efda2c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50584511"
---
# <a name="tlbid"></a>tlbid

**C++-spezifisch**

Ermöglicht das Laden anderer Bibliotheken als der primären Typbibliothek.

## <a name="syntax"></a>Syntax

```
tlbid(number)
```

### <a name="parameters"></a>Parameter

*Anzahl*<br/>
Die Nummer der Typbibliothek in `filename`.

## <a name="remarks"></a>Hinweise

Wenn mehrere Typbibliotheken in einer DLL, es ist möglich, beim Laden von Bibliotheken als die primäre Typbibliothek mit basieren **Tlbid**.

Zum Beispiel:

```cpp
#import <MyResource.dll> tlbid(2)
```

identisch mit folgendem Ausdruck:

```cpp
LoadTypeLib("MyResource.dll\\2");
```

**Ende C++-spezifisch**

## <a name="see-also"></a>Siehe auch

[#import-Attribute](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import-Anweisung](../preprocessor/hash-import-directive-cpp.md)