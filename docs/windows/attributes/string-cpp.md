---
title: Zeichenfolge (C++-COM-Attribut)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.string
helpviewer_keywords:
- string attribute
ms.assetid: ddde900a-2e99-4fcd-86e8-57e1bdba7c93
ms.openlocfilehash: 8bf708067341ecde4fb18d565b7d72866312decd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50603189"
---
# <a name="string-c"></a>string (C++)

Gibt an, dass das eindimensionale **Char**, **"wchar_t"**, `byte` (oder Äquivalent) Array oder der Zeiger auf ein solches Array muss als Zeichenfolge behandelt werden.

## <a name="syntax"></a>Syntax

```cpp
[string]
```

## <a name="remarks"></a>Hinweise

Die **Zeichenfolge** C++-Attribut hat die gleiche Funktionalität wie die [Zeichenfolge](/windows/desktop/Midl/string) MIDL-Attribut.

## <a name="example"></a>Beispiel

Der folgende Code zeigt, wie Sie mit **Zeichenfolge** auf eine Schnittstelle und eine Typdefinition:

```cpp
// cpp_attr_ref_string.cpp
// compile with: /LD
#include "unknwn.h"
[module(name="ATLFIRELib")];
[export, string] typedef char a[21];
[dispinterface, restricted, uuid("00000000-0000-0000-0000-000000000001")]
__interface IFireTabCtrl
{
   [id(1)] HRESULT Method3([in, string] char *pC);
};
```

## <a name="requirements"></a>Anforderungen

### <a name="attribute-context"></a>Attributkontext

|||
|-|-|
|**Betrifft**|Array oder Zeiger auf ein Array, das Parameter für die, die Schnittstellenmethode|
|**Wiederholbar**|Nein|
|**Erforderliche Attribute**|Keiner|
|**Ungültige Attribute**|Keiner|

Weitere Informationen zu den Attributkontexten finden Sie unter [Attributkontexte](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>Siehe auch

[IDL-Attribute](idl-attributes.md)<br/>
[Arrayattribute](array-attributes.md)<br/>
[export](export.md)