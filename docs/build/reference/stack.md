---
title: /STACK
ms.date: 11/04/2016
f1_keywords:
- /stack
helpviewer_keywords:
- -STACK editbin option
- STACK editbin option
- stack, setting size
- /STACK editbin option
ms.assetid: a39bcff0-c945-4355-80cc-8e4f24a5f142
ms.openlocfilehash: 89591a9d0a7f19422275b6bce6f4c5a7a723e800
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50647705"
---
# <a name="stack"></a>/STACK

```
/STACK:reserve[,commit]
```

## <a name="remarks"></a>Hinweise

Diese Option legt die Stapelgröße in Bytes fest und akzeptiert Argumente in der Schreibweise von "decimal" oder C-Sprachen. Die Stapelgröße-Option gilt nur für eine ausführbare Datei.

Die *reservieren* Argument gibt die gesamte stapelzuordnung im virtuellen Speicher. EDITBIN rundet den angegebenen Wert in die nächsten 4 Bytes ab.

Der optionale `commit` -Argument interpretiert, die vom Betriebssystem wird. In Windows NT, Windows 95 und Windows 98 `commit` gibt die Menge an physikalischem Arbeitsspeicher, zu einem Zeitpunkt zuordnen. Die Zusicherung von virtuellem Speicher bewirkt die Belegung von Speicher in der Auslagerungsdatei. Eine höhere `commit` -Wert spart Zeit, wenn die Anwendung mehr Stapelspeicher benötigt, erhöht aber die arbeitsspeicheranforderungen und möglicherweise die Startzeit.

## <a name="see-also"></a>Siehe auch

[EDITBIN-Optionen](../../build/reference/editbin-options.md)