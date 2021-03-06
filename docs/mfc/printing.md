---
title: Drucken
ms.date: 11/04/2016
helpviewer_keywords:
- view classes [MFC], print operations
- documents [MFC], printing
- printing [MFC], from framework
- printing [MFC]
ms.assetid: be465e8d-b0c9-4fc5-9fa8-d10486064f76
ms.openlocfilehash: 88b89ee54ec6270b01859d0f0baeea0efebd9ad6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50589389"
---
# <a name="printing"></a>Drucken

Microsoft Windows implementiert geräteunabhängige anzeigen. In MFC, dies bedeutet, dass die gleichen zeichnen-Aufrufe, in der `OnDraw` Memberfunktion der Klasse anzeigen, sind verantwortlich für das Zeichnen auf die Anzeige und auf anderen Geräten, wie z. B. Drucker. Für die Seitenansicht ist das Zielgerät eine simulierte Drucker, auf dem Bildschirm ausgegeben.

##  <a name="_core_your_role_in_printing_vs.._the_framework.92.s_role"></a> Ihre Rolle beim Drucken im Vergleich zu die Framework Rolle

Die Ansichtsklasse hat die folgenden Verantwortungen:

- Informieren Sie das Framework, wie viele Seiten im Dokument sind.

- Wenn Sie aufgefordert, eine angegebene Seite gedruckt, zeichnen Sie diesen Teil des Dokuments.

- Die Zuordnung, und heben Sie die Zuordnung alle Schriftarten oder andere Graphics Device Interface (GDI) Ressourcen, die für das Drucken benötigten.

- Bei Bedarf zu senden alle umschaltcodes, die erforderlich sind, den Druckermodus zu ändern, bevor Sie eine bestimmte Seite, z. B. drucken, um die Drucken Ausrichtung auf einer Basis pro Seite ändern.

Die Framework Aufgaben sind wie folgt aus:

- Anzeigen der **Drucken** Dialogfeld.

- Erstellen Sie eine [CDC](../mfc/reference/cdc-class.md) Objekt für den Drucker.

- Rufen Sie die [StartDoc](../mfc/reference/cdc-class.md#startdoc) und [EndDoc](../mfc/reference/cdc-class.md#enddoc) Memberfunktionen der `CDC` Objekt.

- Wiederholt Aufrufen der [StartPage](../mfc/reference/cdc-class.md#startpage) Memberfunktion die `CDC` Objekt, informiert die View-Klasse, welche Seite gedruckt werden soll, und rufen, die [EndPage](../mfc/reference/cdc-class.md#endpage) Memberfunktion die `CDC` Objekt.

- Rufen Sie überschreibbare-Funktionen in der Ansicht zum richtigen Zeitpunkt.

In den folgenden Artikeln wird erläutert, wie das Framework drucken und Druckvorschau unterstützt:

### <a name="what-do-you-want-to-know-more-about"></a>Was möchten Sie mehr erfahren

- [Wie standarddrucks](../mfc/how-default-printing-is-done.md)

- [Mehrseitige Dokumente](../mfc/multipage-documents.md)

- [Kopf- und Fußzeilen](../mfc/headers-and-footers.md)

- [Zuordnen von GDI-Ressourcen für Drucken](../mfc/allocating-gdi-resources.md)

- [Seitenansicht](../mfc/print-preview-architecture.md)

## <a name="see-also"></a>Siehe auch

[Drucken und Druckvorschau](../mfc/printing-and-print-preview.md)

