---
title: Anzeigen und Verändern von Daten in einem Formular
ms.date: 11/04/2016
helpviewer_keywords:
- forms [C++], displaying data
- displaying data [C++], forms
- ODBC [C++], forms
- record views [C++], displaying data
- data [MFC]
- data [MFC], displaying in a form
ms.assetid: c56185c4-12cb-40b1-b499-02b29ea83e3a
ms.openlocfilehash: 1694d9cbc770e02c550891fc83c1cc0a9f64824a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50517792"
---
# <a name="displaying-and-manipulating-data-in-a-form"></a>Anzeigen und Verändern von Daten in einem Formular

Viele formularbasierten datenzugriffsanwendungen Daten auswählen und in die Felder in einem Formular angezeigt wird. Die Datenbankklasse [CRecordView](../../mfc/reference/crecordview-class.md) bietet Ihnen eine [CFormView](../../mfc/reference/cformview-class.md) Objekt direkt mit einem Recordset-Objekt verbunden. Verwendet die Datensatzansicht [Dialogdatenaustausch (DDX)](../../mfc/dialog-data-exchange-and-validation.md) um die Werte der Felder des aktuellen Datensatzes aus dem Recordset in die Steuerelemente im Formular zu verschieben und aktualisierte Informationen zurück, das Recordset zu verschieben. Das Recordset verwendet im Gegenzug Datensatzfeldaustausch (RFX) zum Verschieben von Daten zwischen der Felddatenmember und die entsprechenden Spalten in einer Tabelle in der Datenquelle.

Sie können den Assistenten zum MFC-Anwendungen verwenden oder **Klasse hinzufügen** (wie in beschrieben [Hinzufügen eines MFC-ODBC-Consumers](../../mfc/reference/adding-an-mfc-odbc-consumer.md)) die View-Klasse und ihrer zugehörigen Recordset-Klasse in Verbindung zu erstellen.

Der Datensatzansicht und dessen Recordset werden zerstört, wenn Sie das Dokument zu schließen. Weitere Informationen zu Datensatzansichten finden Sie unter [Datensatzansichten](../../data/record-views-mfc-data-access.md). Weitere Informationen über RFX finden Sie unter [Datensatzfeldaustausch (RFX)](../../data/odbc/record-field-exchange-rfx.md).

## <a name="see-also"></a>Siehe auch

[ODBC und MFC](../../data/odbc/odbc-and-mfc.md)