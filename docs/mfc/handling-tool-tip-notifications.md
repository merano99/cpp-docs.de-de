---
title: Behandeln von QuickInfo-Benachrichtigungen
ms.date: 11/04/2016
helpviewer_keywords:
- TOOLTIPTEXT structure [MFC]
- CToolBarCtrl class [MFC], handling notifications
- notifications [MFC], tool tips
- tool tips [MFC], notifications
ms.assetid: ddb93b5f-2e4f-4537-8053-3453c86e2bbb
ms.openlocfilehash: 973c4a12f3b3bdc91269736874b7193130290a76
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50548914"
---
# <a name="handling-tool-tip-notifications"></a>Behandeln von QuickInfo-Benachrichtigungen

Bei Angabe der **TBSTYLE_TOOLTIPS** Stil, der Symbolleiste erstellt und verwaltet ein QuickInfo-Steuerelement. Eine QuickInfo ist ein kleines Popupfenster, das eine Textzeile, beschreibt eine Symbolleisten-Schaltfläche enthält. Die QuickInfo wird ausgeblendet, angezeigt werden, nur, wenn der Benutzer platziert den Cursor für eine Symbolleisten-Schaltfläche und bewirkt, dass sie es für ca. eine halbe Sekunde. Die QuickInfo wird neben dem Cursor angezeigt.

Bevor die QuickInfo angezeigt wird, die **TTN_NEEDTEXT** -Nachricht wird auf der Symbolleiste des Fensters den beschreibenden Text für die Schaltfläche mit den abzurufenden gesendet. Wenn auf der Symbolleiste des Fensters ein `CFrameWnd` Fenster Tool-Tipps ohne jegliche zusätzliche Anstrengung, angezeigt werden, da `CFrameWnd` verfügt über eine Standard-Handler für die **TTN_NEEDTEXT** Benachrichtigung. Wenn die besitzende Fenster der Symbolleiste auf die nicht von abgeleitet ist `CFrameWnd`, z. B. ein Dialogfeld oder Formular anzeigen, müssen Sie das Hinzufügen eines Eintrags zur meldungszuordnung Ihres Besitzerfensters und bieten einen Benachrichtigungshandler in der meldungszuordnung. Der Eintrag zur meldungszuordnung Ihres Besitzerfensters lautet wie folgt aus:

[!code-cpp[NVC_MFCControlLadenDialog#40](../mfc/codesnippet/cpp/handling-tool-tip-notifications_1.cpp)]

## <a name="remarks"></a>Hinweise

*memberFxn*<br/>
Die Memberfunktion aufgerufen werden, wenn der Text für diese Schaltfläche benötigt wird.

Beachten Sie, dass die Id der QuickInfo immer 0.

Zusätzlich zu den **TTN_NEEDTEXT** Benachrichtigung ein QuickInfo-Steuerelement kann die folgenden Benachrichtigungen senden zu einem Toolbar-Steuerelement:

|benachrichtigungs-|Bedeutung|
|------------------|-------------|
|**TTN_NEEDTEXTA**|QuickInfo-Steuerelement erfordert ASCII-Text (nur Windows 95)|
|**TTN_NEEDTEXTW**|QuickInfo-Steuerelement erfordert UNICODE-Text (nur Windows NT)|
|**TBN_HOTITEMCHANGE**|Gibt an, dass das "heiß" (hervorgehobene) Element geändert wurde.|
|**NM_RCLICK**|Gibt an, dass der Benutzer eine Schaltfläche mit der rechten Maustaste hat.|
|**TBN_DRAGOUT**|Gibt an, der Benutzer auf die Schaltfläche geklickt hat, und ziehen den Zeiger der Schaltfläche weg. Es kann es sich um eine Anwendung zum Implementieren von Drag und drop aus einer Symbolleisten-Schaltfläche. Beim Empfang dieser Benachrichtigung die Anwendung beginnt das Drag und drop-Vorgangs.|
|**TBN_DROPDOWN**|Gibt an, der Benutzer geklickt hat eine Schaltfläche, verwendet der **TBSTYLE_DROPDOWN** Stil.|
|**TBN_GETOBJECT**|Gibt an, der Benutzer den Zeiger verschoben, über eine Schaltfläche, verwendet der **TBSTYLE_DROPPABLE** Stil.|

Eine Beispiel-Funktion und Weitere Informationen zu QuickInfos finden Sie [QuickInfos](../mfc/tool-tips-in-windows-not-derived-from-cframewnd.md).

## <a name="see-also"></a>Siehe auch

[Verwenden von CToolBarCtrl](../mfc/using-ctoolbarctrl.md)<br/>
[Steuerelemente](../mfc/controls-mfc.md)

