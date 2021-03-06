---
title: Ändern der Schriftart von Text in einem Bild (Bildbearbeitung für Symbole)
ms.date: 11/04/2016
helpviewer_keywords:
- fonts, changing on an image
ms.assetid: b8849d40-d401-4e06-808f-e615cb2bee3b
ms.openlocfilehash: 2bbd8096a2957099acc8c06d501f3ad407b9a974
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50495523"
---
# <a name="changing-the-font-of-text-on-an-image-image-editor-for-icons"></a>Ändern der Schriftart von Text in einem Bild (Bildbearbeitung für Symbole)

Das folgende Verfahren ist ein Beispiel an:

- Hinzufügen von Text auf ein Symbol in einer Windows-Anwendung

- Bearbeiten der Schriftart von text

### <a name="to-change-the-font-of-text-on-an-image"></a>Ändern die Schriftart von Text in einem Bild

1. Erstellen einer C++-Windows Forms-Anwendung. Weitere Informationen finden Sie unter [Erstellen eines Windows-Anwendungsprojekts](/previous-versions/visualstudio/visual-studio-2010/42wc9kk5). Ein `app.ico` Datei wird standardmäßig zum Projekt hinzugefügt.

2. In **Projektmappen-Explorer**, doppelklicken Sie auf die Datei app.ico. Die [Bildbearbeitung](../windows/image-editor-for-icons.md) wird geöffnet.

3. Von der **Image** , wählen Sie im Menü **Tools** und wählen Sie dann **Texttool**. Die [Text Texttool (Dialogfeld)](../windows/text-tool-dialog-box-image-editor-for-icons.md) wird angezeigt.

4. In der **Texttool** (Dialogfeld), Typ `C++` in den leeren Textbereich. Dieser Text wird angezeigt, in einem in der Größe veränderbaren befindet sich in der oberen linken Ecke des `app.ico`in die **Bildbearbeitung**.

5. In der **Bildbearbeitung**, ziehen Sie das Kontrollkästchen in der Größe veränderbaren in der Mitte des app.ico, um die Lesbarkeit von Text zu verbessern.

6. In der **Texttool** Dialogfeld klicken Sie auf die **Schriftart** Schaltfläche. Die [Schriftart für Texttool (Dialogfeld)](../windows/text-tool-font-dialog-box-image-editor-for-icons.md) wird angezeigt.

7. In der **Schriftart für Texttool** wählen Sie im Dialogfeld **Times New Roman** aus der Liste der verfügbaren Schriftarten, die in aufgeführt sind die **Schriftart** Listenfeld.

8. Wählen Sie **fett** aus der Liste der verfügbaren Schriftschnitte aufgeführt, die der **Schriftschnitt** Listenfeld.

9. Wählen Sie **10** zeigen Sie auf der Liste der verfügbaren Größen der **Größe** Listenfeld.

10. Klicken Sie auf die **OK** Schaltfläche. Die **Schriftart für Texttool** wird das Dialogfeld zu schließen und die schriftarteinstellungen der neuen in den Text gelten.

11. Klicken Sie auf die **schließen** Schaltfläche der **Texttool** Dialogfeld. Das Feld mit veränderbarer Größe, um den Text nicht mehr auf die **Bildbearbeitung**.

## <a name="see-also"></a>Siehe auch

[Bearbeiten von Grafischen Ressourcen](../windows/editing-graphical-resources-image-editor-for-icons.md)<br/>
[Symbolleiste](../windows/toolbar-image-editor-for-icons.md)