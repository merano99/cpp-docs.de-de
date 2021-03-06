---
title: 'Symbole und Cursor: Bildressourcen für Anzeigegeräte (Bildbearbeitung für Symbole C++)'
ms.date: 11/04/2016
f1_keywords:
- vc.editors.icon
helpviewer_keywords:
- cursors [C++], creating
- image resources [C++], display devices
- icons [C++], creating
- cursors [C++], types
- icons [C++]
- Image editor [C++], icons and cursors
- cursors [C++]
- display devices [C++], creating icons for
- cursors [C++], hot spots
- icons [C++], types
ms.assetid: 8f0809a8-0cf0-4da9-b23d-51f28bf15f5b
ms.openlocfilehash: 91de1351b3e41701d302d290533b60d4fe791b80
ms.sourcegitcommit: b032daf81cb5fdb1f5a988277ee30201441c4945
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51693008"
---
# <a name="icons-and-cursors-image-resources-for-display-devices-c-image-editor-for-icons"></a>Symbole und Cursor: Bildressourcen für Anzeigegeräte (Bildbearbeitung für Symbole C++)

Symbole und Cursor sind grafische Ressourcen, die mehrere Bilder in verschiedenen Größen und Farbschemas für verschiedene Arten von Anzeigegeräten enthalten können. Außerdem weist ein Cursor einen „Hotspot“ auf, den Ort, den Windows zum Nachverfolgen seiner Position verwendet. Sowohl Symbole und Cursor werden erstellt und bearbeitet, mithilfe der **Image** -Editor wie Bitmaps und andere Bilder auch.

Bei der Erstellung eines neuen Symbols oder Cursors, der **Image** Editor erstellt zunächst ein Bild eines Standardtyps. Das Bild ist anfänglich mit der Bildschirmfarbe (transparent) gefüllt. Wenn es sich bei dem Bild um einen Cursor handelt, befindet sich der Hotspot anfangs in der oberen linken Ecke (Koordinaten 0,0).

In der Standardeinstellung die **Image** -Editor unterstützt die Erstellung weiterer Bilder für die Geräte, die in der folgenden Tabelle gezeigt. Sie können Bilder für andere Geräte erstellen, indem Sie im Dialogfeld [Benutzerdefiniertes Bild](custom-image-dialog-box-image-editor-for-icons.md)die Parameter für Breite, Höhe und Anzahl der Farben eingeben.

> [!NOTE]
> Mithilfe der **Bildbearbeitung**, können Sie die 32-Bit-Images anzeigen, aber nicht bearbeiten.

|Farbe|Breite (in Pixel)|Höhe (in Pixel)|
|-----------|----------------------|-----------------------|
|Monochrom|16|16|
|Monochrom|32|32|
|Monochrom|48|48|
|Monochrom|64|64|
|Monochrom|96|96|
|16|16|16|
|16|32|32|
|16|64|64|
|16|48|48|
|16|96|96|
|256|16|16|
|256|32|32|
|256|48|48|
|256|64|64|
|256|96|96|

- [Erstellen eines neuen Bilds für ein Gerät (Symbol oder Cursor)](../windows/creating-a-device-image-image-editor-for-icons.md)

- [Hinzufügen eines Bildes für ein anderes Anzeigegerät](../windows/adding-an-image-for-a-different-display-device-image-editor-for-icons.md)

- [Kopieren eines Gerätebildes](../windows/copying-a-device-image-image-editor-for-icons.md)

- [Löschen eines Gerätebildes](../windows/deleting-a-device-image-image-editor-for-icons.md)

- [Erstellen transparenter oder invertierter Bereiche in Gerätebildern](../windows/creating-transparent-or-inverse-regions-in-device-images.md)

- [Erstellen eines Symbols oder Cursors mit 256 Farben](creating-a-256-color-icon-or-cursor-image-editor-for-icons.md)

- [Festlegen des Hotspots eines Cursors](../windows/setting-a-cursor-s-hot-spot-image-editor-for-icons.md)

Informationen zum Hinzufügen von Ressourcen zu verwalteten Projekten finden Sie unter [Ressourcen in Desktop-Apps](/dotnet/framework/resources/index) in die *(.NET Framework Developer's Guide*. Weitere Informationen zum manuellen Hinzufügen von Ressourcendateien zu verwalteten Projekten, den Zugriff auf Ressourcen, zum Anzeigen statischer Ressourcen und Zuweisen von Ressourcenzeichenfolgen zu Eigenschaften, finden Sie unter [Erstellen von Ressourcendateien für Desktop-Apps](/dotnet/framework/resources/creating-resource-files-for-desktop-apps). Weitere Informationen zur Globalisierung und Lokalisierung von Ressourcen in verwalteten apps finden Sie unter [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index).

## <a name="requirements"></a>Anforderungen

Keiner

## <a name="see-also"></a>Siehe auch

[Bildbearbeitung für Symbole](../windows/image-editor-for-icons.md)<br/>
[Symbole](/windows/desktop/menurc/icons)<br/>
[Cursor](/windows/desktop/menurc/cursors)