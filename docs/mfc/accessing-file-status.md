---
title: Zugreifen auf den Dateistatus
ms.date: 11/04/2016
helpviewer_keywords:
- files [MFC], status information
- examples [MFC], file status
- files [MFC], accessing
- file status [MFC]
- status of files [MFC]
ms.assetid: 1b8891d6-eb0f-4037-a837-4928fe595222
ms.openlocfilehash: 3e16f8b11d17cd911646c3c9206d1d7deb577ef9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50629787"
---
# <a name="accessing-file-status"></a>Zugreifen auf den Dateistatus

`CFile` unterstützt Sie auch das Abrufen der Status der Datei, z. B., ob die Datei vorhanden ist, Erstellung und Änderung von Datumsangaben und Uhrzeiten, logische Größe und Pfad.

### <a name="to-get-file-status"></a>Zum Abrufen des Dateistatus

1. Verwenden der [CFile](../mfc/reference/cfile-class.md) Klasse zum Abrufen und Festlegen von Informationen zu einer Datei. Eine nützliche Anwendung ist die Verwendung der `CFile` statische Memberfunktion **GetStatus** zu bestimmen, ob eine Datei vorhanden ist. **GetStatus** gibt 0 zurück, wenn die angegebene Datei nicht vorhanden ist.

Daher können Sie das Ergebnis des **GetStatus** zu bestimmen, ob mit der **modeCreate** flag an, wenn das Öffnen einer Datei, wie im folgenden Beispiel gezeigt:

[!code-cpp[NVC_MFCFiles#3](../atl-mfc-shared/reference/codesnippet/cpp/accessing-file-status_1.cpp)]

Weitere Informationen finden Sie unter [Serialisierung](../mfc/serialization-in-mfc.md).

## <a name="see-also"></a>Siehe auch

[Dateien](../mfc/files-in-mfc.md)

