---
title: 'Vorgehensweise: Ändern von Sprache oder Bedingung einer Ressource während des Kopiervorgangs (C++)'
ms.date: 11/04/2016
f1_keywords:
- vc.resvw.resource.changing
helpviewer_keywords:
- Language property [C++]
ms.assetid: 8f622ab0-bac2-468f-ae70-78911afc4759
ms.openlocfilehash: 42d8fb36dcbd243b0a99f2dbc597bdf352f47266
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50642519"
---
# <a name="how-to-change-the-language-or-condition-of-a-resource-while-copying-c"></a>Vorgehensweise: Ändern von Sprache oder Bedingung einer Ressource während des Kopiervorgangs (C++)

Beim Kopieren in eine Ressource können Sie ihre Sprachen- und/oder Bedingungseigenschaft ändern.

- Die Ressourcensprache ermittelt lediglich die Sprache für die Ressource. Dies dient der [FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea) können Sie die Ressource zu identifizieren, für die Sie suchen. (Ressourcen können für jede Sprache Unterschiede aufweisen, die nicht mit dem Text zusammenhängen, z. B. Tastenkombinationen, die nur auf einer japanischen Tastatur funktionieren, oder eine Bitmap, die nur für Builds in Chinesisch gilt usw.)

- Die Bedingung einer Ressource stellt ein definiertes Symbol dar, das eine Bedingung angibt, unter der diese bestimmte Ressourcenkopie zu verwenden ist.

Sprache und Bedingung einer Ressource werden im Arbeitsbereichsfenster nach dem Ressourcennamen in Klammern angezeigt. In diesem Beispiel verwendet die Ressource mit dem Namen „IDD_AboutBox“ Finnisch als Sprache und „XX33“ als Bedingung.

```cpp
IDD_AboutBox (Finnish - XX33)
```

### <a name="to-copy-an-existing-resource-and-change-its-language-or-condition"></a>So kopieren Sie eine vorhandene Ressource und ändern die Sprache oder Bedingung

1. In der RC-Datei oder in der [Ressourcenansicht](../windows/resource-view-window.md) Fenster mit der rechten Maustaste in der Ressource, die Sie kopieren möchten.

2. Wählen Sie **Kopie einfügen** aus dem Kontextmenü.

3. In der **Ressourcenkopie** Dialogfeld:

   - Für die **Sprache** Listenfeld, wählen Sie die Sprache.

   - In der **Bedingung** geben die Bedingung.

## <a name="requirements"></a>Anforderungen

Win32

## <a name="see-also"></a>Siehe auch

[Vorgehensweise: Kopieren von Ressourcen](../windows/how-to-copy-resources.md)<br/>
[Ressourcendateien](../windows/resource-files-visual-studio.md)<br/>
[Ressourcen-Editor](../windows/resource-editors.md)