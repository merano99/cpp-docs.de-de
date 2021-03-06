---
title: Bereinigen von Dokumenten und Ansichten
ms.date: 11/04/2016
helpviewer_keywords:
- views [MFC], cleaning up
- documents [MFC], cleaning up
- documents [MFC], closing
ms.assetid: 0c454db2-3644-434d-9e53-8108a7aedfe1
ms.openlocfilehash: 1357a02379a848af23a6f78dee29e5b6adc1efcc
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50653894"
---
# <a name="cleaning-up-documents-and-views"></a>Bereinigen von Dokumenten und Ansichten

Wenn ein Dokument geschlossen wird, ruft das Framework zuerst seine [DeleteContents](../mfc/reference/cdocument-class.md#deletecontents) Member-Funktion. Wenn Sie im Verlauf des Vorgangs des Dokuments, auf dem Heap Arbeitsspeicher zugeordnet `DeleteContents` ist der beste Ort für die Zuordnung aufheben.

> [!NOTE]
>  Sie sollten nicht die Dokumentendaten in der Destruktor des Dokuments Zuordnung aufheben. Im Fall einer SDI-Anwendung kann das Document-Objekt wiederverwendet werden.

Sie können eine Ansicht des-Destruktor, um den Arbeitsspeicher freigeben, die, den Sie auf dem Heap reserviert, überschreiben.

## <a name="see-also"></a>Siehe auch

[Initialisieren und Bereinigen von Dokumenten und Ansichten](../mfc/initializing-and-cleaning-up-documents-and-views.md)

