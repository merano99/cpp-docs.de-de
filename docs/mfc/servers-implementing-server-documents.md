---
title: 'Server: Implementieren von Serverdokumenten'
ms.date: 11/04/2016
helpviewer_keywords:
- OLE server applications [MFC], managing server documents
- OLE server applications [MFC], implementing OLE servers
- servers, server documents
- server documents [MFC], implementing
ms.assetid: cca1451a-ad09-47ed-b56e-bccd78fc86d1
ms.openlocfilehash: 17c90eb6350a2bf3cd5b695a99dea954dd89a033
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50436490"
---
# <a name="servers-implementing-server-documents"></a>Server: Implementieren von Serverdokumenten

Dieser Artikel beschreibt die Schritte, die Sie ausführen müssen, um erfolgreich Serverdokument zu implementieren, wenn Sie nicht die OLE-Serveroption im Anwendungs-Assistenten angegeben haben.

#### <a name="to-define-a-server-document-class"></a>So definieren Sie eine Server-Dokument-Klasse

1. Leiten Sie die Dokumentklasse aus `COleServerDoc` anstelle von `CDocument`.

1. Erstellen Sie eine Server-Element-Klasse abgeleitet `COleServerItem`.

1. Implementieren der `OnGetEmbeddedItem` Memberfunktion die Dokumentklasse Server.

   `OnGetEmbeddedItem` wird aufgerufen, wenn der Benutzer eine containeranwendung erstellt oder ein eingebettetes Element bearbeitet. Es sollte ein Element, das gesamte Dokument darstellt, zurück. Dies sollte es sich um ein Objekt von Ihr `COleServerItem`-abgeleitete Klasse.

1. Überschreiben der `Serialize` Memberfunktion versucht, den Inhalt des Dokuments serialisieren. Sie müssen nicht die Liste der Serverelemente serialisiert, es sei denn, Sie sie mithilfe die systemeigenen Daten in Ihrem Dokument darstellen. Weitere Informationen finden Sie unter *Berichtsserverelemente implementieren* in diesem Artikel [Server: Serverelemente](../mfc/servers-server-items.md).

Wenn ein Serverdokument erstellt wird, registriert das Framework automatisch das Dokument mit dem OLE-System-DLLs. Dadurch werden die DLLs, die Serverdokumente zu identifizieren.

Weitere Informationen finden Sie unter [COleServerItem](../mfc/reference/coleserveritem-class.md) und [COleServerDoc](../mfc/reference/coleserverdoc-class.md) in die *Klassenbibliotheksreferenz*.

## <a name="see-also"></a>Siehe auch

[Server](../mfc/servers.md)<br/>
[Server: Serverelemente](../mfc/servers-server-items.md)<br/>
[Server: Implementieren eines Servers](../mfc/servers-implementing-a-server.md)<br/>
[Server: Implementieren eines In-Place-Frame-Fensters](../mfc/servers-implementing-in-place-frame-windows.md)

