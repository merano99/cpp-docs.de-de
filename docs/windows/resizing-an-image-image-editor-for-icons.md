---
title: Größenänderungen bei Bildern (Bildbearbeitung für Symbole)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.image.editing
helpviewer_keywords:
- Image editor [C++], resizing images
- graphics [C++], resizing
- images [C++], resizing
- resizing images
ms.assetid: d83a02c4-4dfe-4586-a0df-51a50c2ba71d
ms.openlocfilehash: 721a8f1de511c105df5d72bbe60685d210ad5a94
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50576097"
---
# <a name="resizing-an-image-image-editor-for-icons"></a>Größenänderungen bei Bildern (Bildbearbeitung für Symbole)

Das Verhalten der **Image** -Editor beim Ändern der Bildgröße, hängt davon ab, ob Ihr [ausgewählten](../windows/selecting-an-area-of-an-image-image-editor-for-icons.md) das gesamte Bild oder nur eines Teils davon.

Wenn die Auswahl nur einen Teil des Bilds, enthält die **Image** Editor reduziert die Auswahl durch Löschen von Zeilen oder Spalten von Pixeln, und füllen die frei werdenden Regionen mit der aktuellen Hintergrundfarbe aus, oder sie Streckung der Auswahl von Duplizieren von Zeilen oder Spalten von Pixeln.

Wenn die Auswahl auf das gesamte Bild, enthält die **Image** Editor entweder verkleinert und das Bild wird gestreckt oder schneidet und erweitert ihn.

Es gibt zwei Mechanismen zum Ändern der Bildgröße: Ziehpunkte und [Fenster "Eigenschaften"](/visualstudio/ide/reference/properties-window). Sie können den Ziehpunkt zum Ändern der Größe des gesamten oder einen Teil eines Images ziehen. Ziehpunkte, die Sie ziehen können, sind gefüllt. Sie können keine Handles ziehen, die leer sind. Sie können die **Eigenschaften** Fenster zum Ändern der Größe des gesamtes image nur nicht für eine ausgewählte Komponente.

![Ziehpunkte in einer Bitmap](../mfc/media/vcimageeditorsizinghandles.gif "VcImageEditorSizingHandles")<br/>
Ziehpunkte

> [!NOTE]
> Wenn man die **Kachel Raster** gewählten Option in der [Rastereinstellungen (Dialogfeld)](../windows/grid-settings-dialog-box-image-editor-for-icons.md), klicken Sie dann Ändern der Größe von Snapshots an der nächsten Kachel. Wenn nur die **Pixelraster** Option ist aktiviert (Standardeinstellung), Ändern der Größe von Snapshots und dem nächsten verfügbaren Pixel.

- [Größenänderung eines ganzen Bilds](../windows/resizing-an-entire-image-image-editor-for-icons.md)

- [Abschneiden oder Erweitern eines ganzen Bildes](cropping-or-extending-an-entire-image-image-editor-for-icons.md)

- [Verkleinern oder Strecken eines ganzen Bildes](../windows/shrinking-or-stretching-an-entire-image-image-editor-for-icons.md)

- [Verkleinern oder Strecken eines Teiles eines Bildes](../windows/shrinking-or-stretching-part-of-an-image-image-editor-for-icons.md)

Informationen zum Hinzufügen von Ressourcen zu verwalteten Projekten finden Sie unter [Ressourcen in Desktop-Apps](/dotnet/framework/resources/index) in die *(.NET Framework Developer's Guide*. Weitere Informationen zum manuellen Hinzufügen von Ressourcendateien zu verwalteten Projekten, den Zugriff auf Ressourcen, zum Anzeigen statischer Ressourcen und Zuweisen von Ressourcenzeichenfolgen zu Eigenschaften, finden Sie unter [Erstellen von Ressourcendateien für Desktop-Apps](/dotnet/framework/resources/creating-resource-files-for-desktop-apps). Weitere Informationen zur Globalisierung und Lokalisierung von Ressourcen in verwalteten apps finden Sie unter [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index).

## <a name="requirements"></a>Anforderungen

Keiner

## <a name="see-also"></a>Siehe auch

[Zugriffstasten](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[Bearbeiten von Grafischen Ressourcen](../windows/editing-graphical-resources-image-editor-for-icons.md)<br/>
[Bildbearbeitung für Symbole](../windows/image-editor-for-icons.md)