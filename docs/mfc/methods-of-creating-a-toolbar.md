---
title: Methoden zum Erstellen einer Symbolleiste
ms.date: 11/04/2016
helpviewer_keywords:
- CToolBarCtrl class [MFC], and CToolBar class [MFC]
- CToolBar class [MFC], creating toolbars
- MFC toolbars
- toolbar controls [MFC]
- toolbar controls [MFC], creating
- CToolBarCtrl class [MFC], creating toolbars
ms.assetid: f19d8d65-d49f-445c-abe8-d47d3e4101c8
ms.openlocfilehash: 5296c0454e035770e196c3d6a4d15291d0c4ca6c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50612458"
---
# <a name="methods-of-creating-a-toolbar"></a>Methoden zum Erstellen einer Symbolleiste

MFC stellt zwei Klassen zum Erstellen von Symbolleisten: [CToolBar](../mfc/reference/ctoolbar-class.md) und [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md) (die dient als Wrapper für die allgemeine Windows-Steuerungs-API). `CToolBar` Stellt die gesamte Funktionalität des allgemeinen Symbolleisten-Steuerelements, und viele der erforderlichen steuerelementeinstellungen für allgemeine und Strukturen für Sie; verarbeitet die resultierende ausführbare Datei in der Regel werden jedoch größer ist als mit erstellt `CToolBarCtrl`.

`CToolBarCtrl` Ergebnisse in eine kleinere ausführbare Datei, und Sie können in der Regel lieber mit `CToolBarCtrl` , wenn Sie nicht beabsichtigen, auf die Symbolleiste in der MFC-Architektur integriert. Wenn Sie planen, verwenden Sie `CToolBarCtrl` und die Symbolleiste in der MFC-Architektur integriert, müssen Sie zusätzliche Sorgfalt für die Kommunikation von Symbolleisten-Steuerelement Manipulationen mit MFC ausführen. Diese Kommunikation ist nicht schwierig. Es ist jedoch zusätzliche Arbeit, die nicht benötigten ist bei Verwendung von `CToolBar`.

Visual C++ bietet zwei Möglichkeiten, um die allgemeine Symbolleisten-Steuerelement nutzen.

- Erstellen Sie die Symbolleiste mit `CToolBar`, und rufen dann [GetToolBarCtrl](../mfc/reference/ctoolbar-class.md#gettoolbarctrl) für den Zugriff auf die `CToolBarCtrl` Memberfunktionen.

- Erstellen Sie die Symbolleiste mit [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md)Konstruktor.

Beide Methoden erhalten Sie Zugriff auf die Memberfunktionen des Symbolleisten-Steuerelements. Beim Aufruf `CToolBar::GetToolBarCtrl`, es gibt einen Verweis auf eine `CToolBarCtrl` Objekt, damit Sie beide Sätze von Memberfunktionen verwenden können. Finden Sie unter [CToolBar](../mfc/reference/ctoolbar-class.md) Informationen zum Erstellen und zum Erstellen eines neuen Symbolleiste `CToolBar`.

## <a name="see-also"></a>Siehe auch

[Verwenden von CToolBarCtrl](../mfc/using-ctoolbarctrl.md)<br/>
[Steuerelemente](../mfc/controls-mfc.md)

