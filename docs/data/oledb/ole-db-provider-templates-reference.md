---
title: Referenz der OLE DB-Anbietervorlagen
ms.date: 11/04/2016
f1_keywords:
- vc.templates.ole
helpviewer_keywords:
- OLE DB provider templates
ms.assetid: 518358f0-bab1-4de9-bce9-4062cc87c11f
ms.openlocfilehash: b7a90081d342d29be391bdf73f43a82ef4c5fbb5
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556854"
---
# <a name="ole-db-provider-templates-reference"></a>Referenz der OLE DB-Anbietervorlagen

Die Klassen und Schnittstellen für OLE DB-Anbieter-Vorlagen können in folgenden Kategorien gruppiert werden. Das Referenzmaterial enthält zudem Informationen zu den [Makros für OLE DB-Anbietervorlagen](../../data/oledb/macros-for-ole-db-provider-templates.md).

Die Klassen verwenden die folgende Benennungskonvention verwendet: eine Klasse mit dem Muster namens `IWidgetImpl` würde eine Implementierung der Schnittstelle bereitstellen, `IWidget`.

## <a name="session-classes"></a>Sitzungsklassen

[IDBCreateSessionImpl](../../data/oledb/idbcreatesessionimpl-class.md)<br/>
Erstellt eine neue Sitzung über das Datenquellenobjekt, und gibt die angeforderte Schnittstelle zurück, auf die neu erstellte Sitzung. Erforderliche Schnittstelle für Datenquellenobjekte.

[ISessionPropertiesImpl](../../data/oledb/isessionpropertiesimpl-class.md)<br/>
Implementiert die Sitzungseigenschaften durch Aufrufen einer statischen Funktion, die durch die Set-eigenschaftenzuordnung definiert. Die Set-eigenschaftenzuordnung sollte in Ihrer Sitzungsklasse angegeben werden. Erforderliche Schnittstelle für Sitzungen.

## <a name="rowset-classes"></a>Schemarowset-Klassen

[CRowsetImpl](../../data/oledb/crowsetimpl-class.md)

Stellt eine Standardimplementierung der OLE DB-Rowset ohne mehrfache Vererbung von viele Implementierung-Schnittstellen bereit. Die einzige Methode, die für die Sie bereitstellen müssen, ist der Implementierung `Execute`.

[CSimpleRow](../../data/oledb/csimplerow-class.md)<br/>
Stellt eine Standardimplementierung für den Zeilenziehpunkt, die in dient der `IRowsetImpl` Klasse. Ein Zeilenhandle ist logisch ein eindeutiges Tag für eine Ergebniszeile. `IRowsetImpl` erstellt ein neues `CSimpleRow` für jede Zeile im angeforderten `IRowsetImpl::GetNextRows`.

[IAccessorImpl](../../data/oledb/iaccessorimpl-class.md)<br/>
OLE DB verlangt von Anbietern zum Implementieren einer `HACCESSOR`, dies ist ein Tag auf ein Array von `DBBINDING` Strukturen. Bietet `HACCESSOR`s, die Adressen sind die `BindType` Strukturen. Erforderlich für Rowsets und Befehle.

[IColumnsInfoImpl](../../data/oledb/icolumnsinfoimpl-class.md)<br/>
Delegiert an eine statische Funktion, die von der Provider-Spalte-Zuordnung definiert. Erforderliche Schnittstelle für Rowsets und Befehle.

[IConvertTypeImpl](../../data/oledb/iconverttypeimpl-class.md)<br/>
Erhalten Informationen über die Verfügbarkeit von typkonvertierungen für einen Befehl oder in einem Rowset. Erforderlich für Befehle, Rowsets und Indexes-Schemarowsets. Implementiert die `IConvertType` Schnittstelle, indem Sie auf das Konvertierungsobjekt vom OLE DB delegieren.

[IDBSchemaRowsetImpl](../../data/oledb/idbschemarowsetimpl-class.md)<br/>
Implementiert die `IDBSchemaRowset` Schnittstelle und die vorlagenbasierte erstellerfunktion `CreateSchemaRowset`.

[IOpenRowsetImpl](../../data/oledb/iopenrowsetimpl-class.md)<br/>
Öffnet und gibt ein Rowset, das alle Zeilen aus einer einzelnen Basistabelle oder einem Index enthält. Verbindliche Schnittstelle für ein Sitzungsobjekt.

[IRowsetChangeImpl](../../data/oledb/irowsetchangeimpl-class.md)<br/>
Implementiert die OLE DB [IRowsetChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms715790(v=vs.85)) -Schnittstelle, die ermöglicht, der die Werte der Spalten in vorhandenen Zeilen löschen von Zeilen sowie das Einfügen neuer Zeilen aktualisiert.

[IRowsetCreatorImpl](../../data/oledb/irowsetcreatorimpl-class.md)<br/>
Diese Klasse erbt von [IObjectWithSite](/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite) und überschreibt [IObjectWithSite::SetSite](/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite). `IRowsetCreatorImpl` führt die gleichen Funktionen wie `IObjectWithSite` kann jedoch auch die OLE DB-Eigenschaften `DBPROPCANSCROLLBACKWARDS` und `DBPROPCANFETCHBACKWARDS`.

[IRowsetIdentityImpl](../../data/oledb/irowsetidentityimpl-class.md)<br/>
Implementiert die `IRowsetIdentity` -Schnittstelle, die Ihnen die Möglichkeit, verglichen werden soll, ob zwei Zeilen mit Daten identisch oder nicht sind.

[IRowsetImpl](../../data/oledb/irowsetimpl-class.md)<br/>
Stellt eine Implementierung der `IRowset` -Schnittstelle, die die grundlegende Rowset-Schnittstelle ist.

[IRowsetInfoImpl](../../data/oledb/irowsetinfoimpl-class.md)<br/>
Implementiert die Rowset-Eigenschaften mithilfe der Eigenschaft-Zuordnung, die definiert, die in Ihrer Klasse des Befehls festgelegt. Erforderliche Schnittstelle für Rowsets.

[IRowsetLocateImpl](../../data/oledb/irowsetlocateimpl-class.md)<br/>
Implementiert die OLE DB [IRowsetLocate](https://docs.microsoft.com/previous-versions/windows/desktop/ms721190(v=vs.85)) -Schnittstelle, die beliebige Zeilen aus einem Rowset abruft. Stellen Sie zur Unterstützung von OLE DB-Lesezeichen in einem Rowset, das Rowset, das von dieser Klasse erben.

[IRowsetNotifyCP](../../data/oledb/irowsetnotifycp-class.md)<br/>
Broadcast-implementiert Funktionen zum Listener auf dem Verbindungspunkt empfehlen `IID_IRowsetNotify` von Änderungen an den Inhalt des Rowsets. Implementieren von Consumern, die Benachrichtigungen verarbeitet [IRowsetNotify](https://docs.microsoft.com/previous-versions/windows/desktop/ms712959(v=vs.85)) und registrieren Sie ihn auf diesen Verbindungspunkt verweist.

[IRowsetUpdateImpl](../../data/oledb/irowsetupdateimpl-class.md)<br/>
Implementiert die OLE DB [IRowsetUpdate](https://docs.microsoft.com/previous-versions/windows/desktop/ms714401(v=vs.85)) -Schnittstelle, die Consumer die Übertragung von Änderungen mit Verzögerung ermöglicht [IRowsetChange](https://docs.microsoft.com/previous-versions/windows/desktop/ms715790(v=vs.85)) auf die Datenquelle und die Änderungen vor der Übertragung rückgängig zu machen.

## <a name="command-classes"></a>Command-Klassen

[ICommandImpl](../../data/oledb/icommandimpl-class.md)<br/>
Stellt eine Implementierung der `ICommand`-Schnittstelle bereit. Diese Schnittstelle ist nicht sichtbar, aber erfolgt durch `ICommandTextImpl`. Eine erforderliche Schnittstelle für das Command-Objekt.

[ICommandPropertiesImpl](../../data/oledb/icommandpropertiesimpl-class.md)<br/>
Diese Implementierung von der `ICommandProperties` Schnittstelle erfolgt durch eine statische Funktion, die von definiert die `BEGIN_PROPSET_MAP` Makro. Obligatorisch einschaltbefehle.

[ICommandTextImpl](../../data/oledb/icommandtextimpl-class.md)<br/>
Legt fest, speichert und gibt den Befehlstext zurück. Obligatorisch einschaltbefehle.

[IDBCreateCommandImpl](../../data/oledb/idbcreatecommandimpl-class.md)<br/>
Erstellt einen neuen Befehl über das Sitzungsobjekt und gibt die angeforderte Schnittstelle zurück, auf die neu erstellte Befehl. Eine optionale Schnittstelle für Session-Objekte.

Werden von anderen Klassen `IColumnsInfoImpl` und `IAccessorImpl`, die im obigen Abschnitt zu Schemarowset-Klassen beschrieben.

## <a name="data-source-classes"></a>Datenquellenklassen

[IDBInitializeImpl](../../data/oledb/idbinitializeimpl-class.md)<br/>
Erstellt und löscht die Verbindung mit der Consumer. Erforderliche Schnittstelle für Datenquellenobjekte und optionale Schnittstelle für Enumeratoren.

[IDBPropertiesImpl](../../data/oledb/idbpropertiesimpl-class.md)<br/>
`IDBProperties` ist eine erforderliche Schnittstelle für Datenquellenobjekte und eine optionale Schnittstelle für Enumeratoren. Aber wenn Sie einen Enumerator verfügbar macht `IDBInitialize`, verfügbar machen `IDBProperties` (Eigenschaften für die Datenquelle).

[IGetDataSourceImpl](../../data/oledb/igetdatasourceimpl-class.md)<br/>
Ruft einen Schnittstellenzeiger auf das Datenquellenobjekt ab. Erforderliche Schnittstelle für die Sitzung.

## <a name="other-classes"></a>Andere Klassen

[CUtlProps](../../data/oledb/cutlprops-class.md)<br/>
Die Eigenschaften für eine Vielzahl von Schnittstellen für OLE DB-Eigenschaft implementiert (z. B. `IDBProperties`, `ISessionProperties`, und `IRowsetInfo`).

[IErrorRecordsImpl](../../data/oledb/ierrorrecordsimpl-class.md)

Implementiert die OLE DB [IErrorRecords](https://docs.microsoft.com/previous-versions/windows/desktop/ms718112(v=vs.85)) Schnittstelle, Hinzufügen von Einträgen zu und Abrufen von Datensätzen aus einem Datenelement.

## <a name="see-also"></a>Siehe auch

[Referenz der OLE DB-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-reference.md)<br/>
[OLE DB-Vorlagen](../../data/oledb/ole-db-templates.md)