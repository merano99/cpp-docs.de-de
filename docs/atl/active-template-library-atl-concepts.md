---
title: ATL-Konzepte (Active Template Library)
ms.date: 11/04/2016
helpviewer_keywords:
- ATL, about ATL
ms.assetid: a3960991-4d76-4da5-9568-3fa7fde53ff4
ms.openlocfilehash: 9b8c293bc92071509607e8496a5601d0c6ef2018
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50523736"
---
# <a name="active-template-library-atl-concepts"></a>ATL-Konzepte (Active Template Library)

Die Active Template Library (ATL) ist ein Satz von vorlagenbasierter C++-Klassen, mit denen Sie die Objekte für kleine, schnelle Component Object Model (COM) zu erstellen. Sie verfügt über spezielle Unterstützung für wichtige COM-Funktionen, wie z.B. vordefinierte Implementierungen duale Schnittstellen, standard-COM-Enumerator-Schnittstellen, Verbindungspunkte, abtrennbare Schnittstellen und ActiveX-Steuerelemente.

Wenn Sie viele der ATL-Programmierung tun, sollten Sie weitere Informationen zu Attributen, ein neues Feature in Visual C++ .NET, die COM-Programmierung zu vereinfachen. Weitere Informationen finden Sie unter [attributierte Programmierung](../windows/attributed-programming-concepts.md).

## <a name="in-this-section"></a>In diesem Abschnitt

[ATL-Lernprogramm](../atl/active-template-library-atl-tutorial.md)<br/>
Führt Sie durch die Erstellung eines Steuerelements und zeigt einige ATL-Grundlagen im Prozess.

[Einführung in COM und ATL](../atl/introduction-to-com-and-atl.md)<br/>
Stellt die wichtigsten Konzepte hinter das Component Object Model (COM). In diesem Artikel wird auch kurz erläutert, was ATL ist und wann Sie verwendet werden soll.

[Grundlagen von ARL COM-Objekten](../atl/fundamentals-of-atl-com-objects.md)<br/>
Beschreibt die Beziehung zwischen verschiedenen ATL-Klassen und wie diese Klassen implementiert werden.

[Duale Schnittstellen und ATL](../atl/dual-interfaces-and-atl.md)<br/>
Beschreibt die duale Schnittstellen aus Sicht der ATL.

[ATL-Auflistungen und -Enumeratoren](../atl/atl-collections-and-enumerators.md)<br/>
Beschreibt die Implementierung und die Erstellung von Sammlungen und Enumeratoren in ATL

[Grundlagen von zusammengesetzten Steuerelementen](../atl/atl-composite-control-fundamentals.md)<br/>
Bietet schrittweise Anleitungen zum Erstellen eines zusammengesetzten Steuerelements an. Ein zusammengesetztes Steuerelement ist eine Art von ActiveX-Steuerelement, das andere ActiveX-Steuerelemente oder Windows-Steuerelemente enthalten kann.

[Fragen und Antworten zur ATL-Steuerelementkapselung](../atl/atl-control-containment-faq.md)<br/>
Behandelt die grundlegenden Fragen zum Hosten von Steuerelementen mit ATL

[ATL COM-Eigenschaftenseiten](../atl/atl-com-property-pages.md)<br/>
Erfahren Sie, wie Sie angeben, und Implementieren von COM-Eigenschaftenseiten.

[ATL-Unterstützung für DHTML-Steuerelemente](../atl/atl-support-for-dhtml-controls.md)<br/>
Enthält detaillierte Anweisungen zum Erstellen eines DHTML-Steuerelements.

[ATL-Verbindungspunkte](../atl/atl-connection-points.md)<br/>
Erläutert, was die Verbindungspunkte sind und wie diese von ATL implementiert.

[Ereignisbehandlung und ATL](../atl/event-handling-and-atl.md)<br/>
Beschreibt die Schritte, die Sie durchführen müssen, um die Verwendung von ATL COM-Ereignisse behandeln müssen [IDispEventImpl](../atl/reference/idispeventimpl-class.md) und [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md) Klassen.

[ATL und der freethreaded Marshaller](../atl/atl-and-the-free-threaded-marshaler.md)<br/>
Enthält Informationen zu der ATL-Assistent für einfache Objekte die Option aus, die Ihre Klasse die freethreaded Marshaller (FTM) aggregieren kann.

[Angeben des Projekts. Threading-Modell](../atl/specifying-the-threading-model-for-a-project-atl.md)<br/>
Beschreibt die Makros, die zur Steuerung der Leistung zur Laufzeit im Zusammenhang mit threading in Ihrem Projekt verfügbar sind.

[ATL-Modulklassen](../atl/atl-module-classes.md)<br/>
Beschreibt die neuen für ATL 7.0. Modulklassen implementieren die grundlegende Funktionalität, die ATL erforderlich

[ATL-Dienste](../atl/atl-services.md)<br/>
Behandelt die Serie von Ereignissen, die auftreten, wenn ein Dienst implementiert wird. Außerdem spricht über einige Konzepte im Zusammenhang mit der Entwicklung eines Diensts.

[ATL-Fensterklassen](../atl/atl-window-classes.md)<br/>
Beschreibt, wie zum Erstellen, Informationen und Unterklasse-Fenstern in ATL Der ATL-Fensterklassen sind nicht COM-Klassen.

[ATL-Auflistungsklassen](../atl/atl-collection-classes.md)<br/>
Beschreibt, wie Arrays und Zuordnungen in ATL

[Der ATL-Registrierungskomponente (Registrar)](../atl/atl-registry-component-registrar.md)<br/>
Erläutert, ATL-Skripting-Syntax und ersetzbare Parameter. Außerdem wird die Verwendung, um einen statischen Link zur der Registrierungsstelle einzurichten.

[Programmieren mit ATL- und C-Laufzeitcode](../atl/programming-with-atl-and-c-run-time-code.md)<br/>
Erläutert die Vorteile der Verknüpfung von statisch oder dynamisch auf die C Run-Time-Laufzeitbibliothek (CRT).

[Programmieren mit CComBSTR](../atl/programming-with-ccombstr-atl.md)<br/>
Erläutert verschiedene Situationen mit Vorsicht beim Programmieren mit `CComBSTR`.

[Codierungsreferenz](../atl/atl-encoding-reference.md)<br/>
Bietet Funktionen und Makros, die in einen Bereich von allgemeinen Internetstandards wie Uuencode, hexadezimale und UTF8 in atlenc.h unterstützen Codierung.

[Referenz zu Hilfsprogrammen](../atl/atl-utilities-reference.md)<br/>
Stellt Code bereit, für die Bearbeitung von Pfade und URLs in Form von [CPathT](../atl/reference/cpatht-class.md) und [CUrl](../atl/reference/curl-class.md). Einen Threadpool [CThreadPool](../atl/reference/cthreadpool-class.md), in Ihren eigenen Anwendungen verwendet werden kann. Dieser Code finden Sie in "atlpath.h" und "atlutil.h".

## <a name="related-sections"></a>Verwandte Abschnitte

[ATL-Beispiele](../visual-cpp-samples.md)<br/>
Enthält Beschreibungen und Links für die ATL-Beispiel-Programme.

[Erstellen eines ATL-Projekts](../atl/reference/creating-an-atl-project.md)<br/>
Enthält Informationen über ATL-Projektassistenten.

[ATL-Steuerelement-Assistent](../atl/reference/atl-control-wizard.md)<br/>
Erläutert das Hinzufügen von Klassen.

[Attributiertes Programmieren](../windows/attributed-programming-concepts.md)<br/>
Enthält eine Übersicht zur Verwendung von Attributen zur Vereinfachung der COM-Programmierung sowie eine Liste mit Links zu ausführlicheren Themen.

[ATL-Klassenübersicht](../atl/atl-class-overview.md)<br/>
Bietet Informationen und Links zu den ATL-Klassen.

