---
title: _bittest, _bittest64
ms.date: 11/04/2016
f1_keywords:
- _bittest64
- _bittest_cpp
- _bittest64_cpp
- _bittest
helpviewer_keywords:
- _bittest intrinsic
- _bittest64 intrinsic
- bt instruction
ms.assetid: 15e62afb-abea-4ee7-a6b1-13efa2034937
ms.openlocfilehash: 170979b5cf463d72f645599e146d1e8e2a10154d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50645395"
---
# <a name="bittest-bittest64"></a>_bittest, _bittest64

**Microsoft-spezifisch**

Generiert die `bt`-Anweisung, die das Bit an Position `b` der Adresse `a` untersucht, und gibt den Wert dieses Bits zurück.

## <a name="syntax"></a>Syntax

```
unsigned char _bittest(
   long const *a,
   long b
);
unsigned char _bittest64(
   __int64 const *a,
   __int64 b
);
```

### <a name="parameters"></a>Parameter

*a*<br/>
[in] Ein Zeiger auf den zu untersuchenden Speicher.

*b*<br/>
[in] Die zu testende Bitposition.

### <a name="return-value"></a>Rückgabewert

Das Bit an der angegebenen Position.

## <a name="requirements"></a>Anforderungen

|Systemintern|Architektur|Header|
|---------------|------------------|------------|
|`_bittest`|X86, ARM, x64|\<intrin.h>|
|`_bittest64`|ARM, x64|\<intrin.h>|

## <a name="remarks"></a>Hinweise

Diese Routine ist nur als systeminterne Funktion verfügbar.

## <a name="example"></a>Beispiel

```cpp
// bittest.cpp
// processor: x86, ARM, x64

#include <stdio.h>
#include <intrin.h>

long num = 78002;

int main()
{
    unsigned char bits[32];
    long nBit;

    printf_s("Number: %d\n", num);

    for (nBit = 0; nBit < 31; nBit++)
    {
        bits[nBit] = _bittest(&num, nBit);
    }

    printf_s("Binary representation:\n");
    while (nBit--)
    {
        if (bits[nBit])
            printf_s("1");
        else
            printf_s("0");
    }
}
```

```Output
Number: 78002
Binary representation:
0000000000000010011000010110010
```

**Ende Microsoft-spezifisch**

## <a name="see-also"></a>Siehe auch

[Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)