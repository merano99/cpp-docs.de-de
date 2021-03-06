---
title: Verwenden von OLE DB-Datensatzansichten
ms.date: 10/24/2018
helpviewer_keywords:
- OLE DB record views
- COleDBRecordView class, overview
- rowsets, record views
- record views, record view objects
- OLE DB, record views
- MFC, record views
ms.assetid: 1cd3e595-ce08-43d8-a0a9-d03b5d3e24ce
ms.openlocfilehash: 631e78e1a397ec360b1f3b2d94d7340e96925e23
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50582711"
---
# <a name="using-ole-db-record-views"></a>Verwenden von OLE DB-Datensatzansichten

Wenn Sie OLE DB-Rowset-Daten in einer MFC-Anwendung anzeigen möchten, verwenden Sie die MFC-Klasse [COleDBRecordView](../../mfc/reference/coledbrecordview-class.md). Ein Datensatzansichts-Objekt erstellt wird, von `COleDBRecordView` ermöglicht es Ihnen, die Datenbankdatensätze in MFC-Steuerelemente anzuzeigen. Die Datensatzansicht ist ein Dialogfeld Formularansicht können Sie direkt verbunden wird, um ein OLE DB-Rowset-Objekt, das erstellt wird, aus der `CRowset` Vorlagenklasse. Ein Handle für das Rowsetobjekt, das erste ist einfach:

```cpp
COleDBRecordView myRecordView;
...
// CProductAccessor is a user record class
CRowset<CAccessor<CProductAccessor>> myRowSet = myRecordView.OnGetRowset();
```

Die Ansicht zeigt die Felder der `CRowset` Objekt in den Steuerelementen des Dialogfelds. Die `COleDBRecordView` Objekt verwendet (Dialogfeld Data Exchange, DDX) und die Navigationsfunktionen `CRowset` (`MoveFirst`, `MoveNext`, `MovePrev`, und `MoveLast`) um die Verschiebung von Daten zwischen den Steuerelementen im Formular zu automatisieren. und die Felder des Rowsets. `COleDBRecordView` verfolgt des Position des Benutzers im Rowset, damit die Datensatzansicht aktualisieren kann, die Benutzeroberfläche und stellt eine [OnMove](../../mfc/reference/coledbrecordview-class.md#onmove) Methode zum Aktualisieren des aktuellen Datensatzes vor dem Verschieben in einen anderen.

Sie können die DDX-Funktionen mit `COleDbRecordView` um Daten direkt aus dem Datenbankrecordset abrufen und in einem Dialogfeldsteuerelement anzuzeigen. Verwenden der **DDX_** <strong>\*</strong> Methoden (z. B. `DDX_Text`), nicht die **DDX_Field** <strong>\*</strong> ()-Funktionen wie z. B. `DDX_FieldText`) mit `COleDbRecordView`.

## <a name="see-also"></a>Siehe auch

[Verwenden von Zugriffsmethoden](../../data/oledb/using-accessors.md)<br/>
[COleDBRecordView-Klasse](../../mfc/reference/coledbrecordview-class.md)<br/>
