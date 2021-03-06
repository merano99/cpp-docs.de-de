---
title: Verwenden von DropDown-Schaltflächen in einem Symbolleisten-Steuerelement
ms.date: 11/04/2016
f1_keywords:
- TBN_DROPDOWN
- TBSTYLE_EX_DRAWDDARROWS
helpviewer_keywords:
- CToolBarCtrl class [MFC], drop-down buttons
- toolbars [MFC], drop-down buttons
- drop-down buttons in toolbars
- TBSTYLE_EX_DRAWDDARROWS
- TBN_DROPDOWN notification [MFC]
ms.assetid: b859f758-d2f6-40d9-9c26-0ff61993b9b2
ms.openlocfilehash: fe314e0fdff70979dfc858bb89578170f9a9ee02
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50453495"
---
# <a name="using-drop-down-buttons-in-a-toolbar-control"></a>Verwenden von DropDown-Schaltflächen in einem Symbolleisten-Steuerelement

Zusätzlich zur standardmäßigen Schaltflächen haben eine Symbolleiste auch Dropdown-Schaltflächen. Eine Dropdown-Schaltfläche wird in der Regel durch das Vorhandensein einer angefügten Pfeil nach unten angezeigt.

> [!NOTE]
>  Die angefügte Pfeil nach unten wird nur angezeigt, wenn der erweiterte Stil TBSTYLE_EX_DRAWDDARROWS festgelegt wurde.

Wenn der Benutzer klickt auf diesen Pfeil (oder die Schaltfläche selbst, wenn kein Pfeil vorhanden ist), wird eine TBN_DROPDOWN-Benachrichtigung an das übergeordnete Element des der Symbolleisten-Steuerelement gesendet. Sie können diese Benachrichtigung verarbeitet und ein Popupmenü anzuzeigen; ähnlich wie das Verhalten von Internet Explorer.

Das folgende Verfahren veranschaulicht, wie eine Dropdown-Symbolleisten-Schaltfläche mit einem Popup-Menü zu implementieren:

### <a name="to-implement-a-drop-down-button"></a>Implementieren Sie eine Dropdown Schaltfläche

1. Sobald Ihre `CToolBarCtrl` Objekt erstellt wurde, legen Sie den TBSTYLE_EX_DRAWDDARROWS-Stil, mithilfe des folgenden Codes:

   [!code-cpp[NVC_MFCControlLadenDialog#36](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_1.cpp)]

1. Legen Sie den TBSTYLE_DROPDOWN-Stil für alle neu ([InsertButton](../mfc/reference/ctoolbarctrl-class.md#insertbutton) oder [AddButtons](../mfc/reference/ctoolbarctrl-class.md#addbuttons)) oder vorhandenen ([SetButtonInfo](../mfc/reference/ctoolbarctrl-class.md#setbuttoninfo)) Schaltflächen, die Dropdown-Schaltflächen. Im folgende Beispiel wird veranschaulicht, ändern eine vorhandene Schaltfläche in einem `CToolBarCtrl` Objekt:

   [!code-cpp[NVC_MFCControlLadenDialog#37](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_2.cpp)]

1. Fügen Sie einen TBN_DROPDOWN-Handler in der übergeordneten Klasse des Symbolleistenobjekts hinzu.

   [!code-cpp[NVC_MFCControlLadenDialog#38](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_3.cpp)]

1. Zeigen Sie in den neuen Handler auf im entsprechenden Popupmenü. Der folgende Code veranschaulicht eine Methode:

   [!code-cpp[NVC_MFCControlLadenDialog#39](../mfc/codesnippet/cpp/using-drop-down-buttons-in-a-toolbar-control_4.cpp)]

## <a name="see-also"></a>Siehe auch

[Verwenden von CToolBarCtrl](../mfc/using-ctoolbarctrl.md)<br/>
[Steuerelemente](../mfc/controls-mfc.md)

