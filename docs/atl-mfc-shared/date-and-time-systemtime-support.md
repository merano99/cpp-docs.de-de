---
title: 'Datum und Uhrzeit: SYSTEMTIME-Unterstützung'
ms.date: 11/04/2016
f1_keywords:
- SYSTEMTIME
helpviewer_keywords:
- system time
- FILETIME structure, with CTime class
- time [C++], formatting
- SYSTEMTIME structure
- dates [C++], MFC
- formatting [C++], time
ms.assetid: 201528e4-2ffa-48fc-af8f-203aa86d942a
ms.openlocfilehash: e4aac4078ce6d75fb1613c158cdf790f2a596a01
ms.sourcegitcommit: c85c8a1226d8fbbaa29f4691ed719f8e6cc6575c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2019
ms.locfileid: "54893495"
---
# <a name="date-and-time-systemtime-support"></a>Datum und Uhrzeit: SYSTEMTIME-Unterstützung

Die [CTime](../atl-mfc-shared/reference/ctime-class.md) -Klasse verfügt über Konstruktoren, die System- und Dateizeiten von Win32 akzeptieren. Wenn Sie `CTime`-Objekte zu diesem Zweck verwenden, müssen Sie deren Initialisierung entsprechend anpassen, wie in diesem Artikel beschrieben.

Weitere Informationen zur SYSTEMTIME-Struktur finden Sie unter [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime). Weitere Informationen zur FILETIME-Struktur finden Sie unter [FILETIME](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

MFC bietet weiterhin `CTime`-Konstruktoren, die Argumente im MS-DOS-Format akzeptieren. Ab MFC-Version 3.0 unterstützt die `CTime`-Klasse jedoch auch einen Konstruktor, der eine Win32-`SYSTEMTIME`-Struktur akzeptiert, und einen anderen, der eine Win32-`FILETIME`-Struktur akzeptiert.

Die neuen `CTime`-Konstruktoren sind:

- CTime (const SYSTEMTIME & `sysTime`);

- CTime (const FILETIME & `fileTime`);

Die *FileTime* Parameter ist ein Verweis auf eine Win32- `FILETIME` Struktur, die Uhrzeit als 64-Bit-Wert, ein zweckmäßigeres Format für die interne Speicherung als steht eine `SYSTEMTIME` Struktur und das Format von Win32 zur Stellen Sie den Erstellungszeitpunkt der Datei dar.

Wenn Ihr Code ein `CTime`-Objekt enthält, das mit der Systemzeit initialisiert wurde, sollten Sie unter Win32 den `SYSTEMTIME`-Konstruktor verwenden.

Verwenden Sie wahrscheinlich nicht `CTime` `FILETIME` -Initialisierung direkt. Bei Verwendung einer `CFile` Objekt, das eine Datei zu manipulieren [CFile:: GetStatus](../mfc/reference/cfile-class.md#getstatus) Timestamp der Datei abgerufen, für die Sie über eine `CTime` Objekt initialisiert wird, mit eine `FILETIME` Struktur.

## <a name="what-do-you-want-to-know-more-about"></a>Was möchten Sie mehr erfahren

- [Allgemeine Datums- und zeitprogrammierung in MFC](../atl-mfc-shared/date-and-time.md)

- [Automatisierungssupport bei der Datums- und zeitprogrammierung](../atl-mfc-shared/date-and-time-automation-support.md)

## <a name="see-also"></a>Siehe auch

[Datum und Uhrzeit](../atl-mfc-shared/date-and-time.md)
