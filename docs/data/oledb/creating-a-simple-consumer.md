---
title: Erstellen eines einfachen Consumers
ms.date: 11/06/2018
helpviewer_keywords:
- OLE DB consumers, creating
ms.assetid: ae32d657-72ea-4db8-9839-75cb5cff68ae
ms.openlocfilehash: 4346bca99d3744657072a4940776934e3c03e9de
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326640"
---
# <a name="creating-a-simple-consumer"></a>Erstellen eines einfachen Consumers

Verwenden der **ATL-Projektassistenten** und **ATL-OLE DB-Consumer-Assistenten** um einen OLE DB-Vorlagen-Consumer zu generieren.

## <a name="to-create-a-console-application-for-an-ole-db-consumer"></a>Zum Erstellen einer Konsolenanwendung für einen OLE DB-consumer

1. Klicken Sie im Menü **Datei** auf **Neu**und dann auf **Projekt**.

   Das Dialogfeld **Neues Projekt** wird angezeigt.

1. In der **Projekttypen** Bereich, klicken Sie auf die **installiert** > **Visual C++** > **Windows Desktop** Ordner und klicken Sie dann auf die **-Assistenten für Windows Desktop** Symbol in der **Vorlagen** Bereich. In der **Namen** Geben Sie den Namen des Projekts, z. B. *MyCons*.

1. Klicken Sie auf **OK**.

   Die **-Projekt für Windows Desktop** -Assistent wird angezeigt.

1. Auf der **Anwendungseinstellungen** Seite **Konsolenanwendung**, und wählen Sie dann **allgemeine Headerdateien für ATL hinzufügen**.

1. Klicken Sie auf **OK** den Assistenten zu schließen und das Projekt zu erstellen.

Verwenden Sie als Nächstes die **ATL-OLE DB-Consumer-Assistenten** zum Hinzufügen eines OLE DB-Consumer-Objekts.

## <a name="to-create-a-consumer-with-the-atl-ole-db-consumer-wizard"></a>Um einen Consumer mit dem ATL-OLE DB-Consumer-Assistenten erstellen

1. In **Projektmappen-Explorer**, mit der rechten Maustaste die `MyCons` Projekt.

1. Klicken Sie im Kontextmenü auf **hinzufügen**, und klicken Sie dann auf **neues Element**.

   Das Dialogfeld **Neues Element hinzufügen** wird angezeigt.

1. In der **Kategorien** Bereich, klicken Sie auf **installiert** > **Visual C++** > **ATL**, klicken Sie auf die **ATL-OLEDB-Consumer** Symbol in der **Vorlagen** , und klicken Sie dann auf **hinzufügen**.

   Die **ATL-OLEDB-Consumer-Assistent** angezeigt wird.

1. Klicken Sie auf die **Datenquelle** Schaltfläche.

   Die **Datenlinkeigenschaften** Dialogfeld wird angezeigt.

1. In der **Datenlinkeigenschaften** Dialogfeld Feld, gehen Sie folgendermaßen vor:

   1. Auf der **Anbieter** Registerkarte, geben Sie einen OLE DB-Anbieter.

   1. Auf der **Verbindung** Registerkarte, geben Sie die erforderliche Informationen, z. B. Servername, Anmelde-ID und Kennwort für die Datenquelle und die Datenbank auf dem Server.

      > [!NOTE]
      > Es wurde ein Sicherheitsproblem mit der **Speichern von Kennwort zulassen** Feature von der **Datenlinkeigenschaften** im Dialogfeld. In **Geben Sie Informationen zum Anmelden an den Server**, es gibt zwei Optionsfelder: **Windows NT integrated Security verwenden** und **bestimmten Benutzernamen und bestimmtes Kennwort**.

      > [!NOTE]
      > Bei Auswahl von **bestimmten Benutzernamen und bestimmtes Kennwort**, Sie haben die Möglichkeit, speichern Sie das Kennwort (mit der **Speichern von Kennwort zulassen** Kontrollkästchen), aber diese Option ist nicht sicher. Es wird empfohlen, die Sie auswählen, **Windows NT integrated Security verwenden**; diese Option verwendet die Windows NT zur Überprüfung Ihrer Identität.

      > [!NOTE]
      > Wenn Sie Windows NT integrated Security verwenden können, sollten Sie eine Anwendung der mittleren Ebene verwenden, um den Benutzer für das Kennwort aufzufordern oder das Kennwort an einem Ort mit Sicherheitsmechanismen, um dessen Schutz zu speichern (nicht im Quellcode).

   1. Nachdem Sie Ihren Anbieter und andere Einstellungen auswählen, klicken Sie auf **Testverbindung** um zu überprüfen, ob die Auswahl auf der vorherigen dialogfeldseiten. Wenn die **Ergebnisse** Feld Berichte `Test connection succeeded`, klicken Sie auf **OK** zum Erstellen der datenverknüpfung.

   Die **Datenbankobjekt auswählen** Dialogfeld wird angezeigt.

1. Verwenden Sie die Strukturansicht-Steuerelement, um eine Tabelle, Sicht oder gespeicherte Prozedur auszuwählen. Wählen Sie für dieses Beispiel die `Products` -Tabelle aus dem `Northwind` Datenbank.

1. Klicken Sie auf **OK**. Wird die **ATL-OLE DB-Consumer-Assistenten**.

1. Der Assistent abgeschlossen ist, die Namen für `Class` und **.h-Datei** basierend auf den Namen der Tabelle, Sicht oder gespeicherte Prozedur, die Sie ausgewählt haben. Sie können diese Namen bearbeiten, wenn Sie möchten.

1. Deaktivieren der **attributiert** Kontrollkästchen, damit der Assistent erstellt der Consumer-Code mit [OLE DB-Vorlagenklassen](../../data/oledb/ole-db-consumer-templates-reference.md) anstelle des standardmäßigen [OLE DB-Consumerattribute](../../windows/ole-db-consumer-attributes.md).

1. Klicken Sie unter **Typ**Option **Befehl**.

   Der Assistent erstellt eine [CCommand](../../data/oledb/ccommand-class.md)--basierten Consumer, wenn Sie die Option **Befehl** oder ein [CTable](../../data/oledb/ctable-class.md)--basierten Consumer, wenn Sie die Option **Tabelle**. Die Tabelle oder Befehlsklasse wird nach dem ausgewählten Objekt mit dem Namen, aber Sie können den Namen bearbeiten.

1. Unter **Unterstützung**, lassen Sie die **Änderung**, **einfügen**, und **löschen** Kontrollkästchen deaktiviert.

   Wählen Sie die **Änderung**, **einfügen**, und **löschen** Kontrollkästchen, um die ändern, einfügen und Löschen von Datensätzen im Rowset zu unterstützen. Weitere Informationen zum Schreiben von Daten an den Daten zu speichern, finden Sie unter [Aktualisieren von Rowsets](../../data/oledb/updating-rowsets.md).

1. Klicken Sie auf **Fertig stellen** an den Consumer zu erstellen.

Der Assistent generiert eine Befehlsklasse und eine Benutzerdatensatz-Klasse, siehe [vom Klassen](../../data/oledb/consumer-wizard-generated-classes.md). Die Befehlsklasse müssen den Namen, den Sie im eingegeben haben die `Class` Feld im Assistenten (in diesem Fall `CProducts`), und die Benutzerdatensatz-Klasse hat einen Namen im Format "*ClassName*Accessor" (in diesem Fall `CProductsAccessor`).

> [!NOTE]
> Der Assistent fügt die folgende Zeile in `Products.h`:

```cpp
#error Security Issue: The connection string may contain a password
```

> [!NOTE]
> Diese Zeile wird verhindert, dass die Consumer-Anwendung zu kompilieren und erinnert Sie daran, Ihre Verbindungszeichenfolge auf der fest programmierte Kennwörter zu überprüfen. Nach dem Überprüfen Ihre Verbindungszeichenfolge enthält, können Sie diese Codezeile entfernen.

## <a name="see-also"></a>Siehe auch

[Erstellen eines OLE DB-Consumers mit einem Assistenten](../../data/oledb/creating-an-ole-db-consumer-using-a-wizard.md)
