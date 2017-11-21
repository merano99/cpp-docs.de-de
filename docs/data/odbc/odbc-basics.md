---
title: "Grundlagen zu ODBC | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ODBC-Komponenten"
  - "ODBC-Komponenten, Erforderliche Komponenten"
  - "ODBC-Cursorbibliothek [ODBC], ODBC-Komponenten"
  - "ODBC, Informationen über ODBC"
  - "ODBC, Komponenten"
ms.assetid: ec529702-0fb2-4754-b8de-d1efa8eca18f
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 10
---
# Grundlagen zu ODBC
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Dieses Thema vermittelt Grundlagen zu ODBC \(Open Database Connectivity\):  
  
-   [Zusammenwirken von ODBC mit den Datenbankklassen](../../data/odbc/odbc-and-the-database-classes.md)  
  
-   [Zusammenwirken von ODBC\-Treibern mit Dynasets](../../data/odbc/odbc-driver-requirements-for-dynasets.md)  
  
-   [ODBC\-Komponenten, die mit den Anwendungen verteilt werden müssen](../../data/odbc/redistributing-odbc-components-to-your-customers.md)  
  
 Sie sollten in diesem Zusammenhang auch das verwandte Thema [ODBC: Die ODBC\-Cursorbibliothek](../../data/odbc/odbc-the-odbc-cursor-library.md) lesen.  
  
> [!NOTE]
>  Auf ODBC\-Datenquellen können Sie über die MFC\-ODBC\-Klassen zugreifen, wie in diesem Thema beschrieben, oder über die MFC\-Datenzugriffsobjekt\-Klassen \(DAO\-Klassen\).  
  
> [!NOTE]
>  Die MFC\-ODBC\-Klassen unterstützen Unicode und Multithreading.  Weitere Informationen über die Multithreadingunterstützung finden Sie unter [ODBC\-Klassen und Threads](../../data/odbc/odbc-classes-and-threads.md).  
  
 ODBC ist ein Call\-Level\-Interface, mit dem Anwendungen auf Daten in jeder beliebigen Datenbank zugreifen können, für die ein ODBC\-Treiber vorhanden ist.  Mithilfe von ODBC können Sie Datenbankanwendungen erstellen, die Zugriff auf jede beliebige Datenbank bieten, für die der Endbenutzer einen ODBC\-Treiber hat.  ODBC stellt eine API zur Verfügung, die es ermöglicht, eine Anwendung unabhängig vom Quell\-Datenbankmanagementsystem \(DBMS\) zu gestalten.  
  
 ODBC ist der datenbankbezogene Teil von WOSA \(Microsoft Windows Open Services Architecture\), einer Schnittstelle, die es Windows\-basierten Desktopanwendungen ermöglicht, Verbindungen zu zahlreichen Computerumgebungen aufzubauen, ohne dass die Anwendung für jede Plattform umgeschrieben werden muss.  
  
 ODBC besteht aus den folgenden Komponenten:  
  
-   ODBC\-API  
  
     Eine Bibliothek mit Funktionsaufrufen, eine Gruppe von Fehlercodes und eine [SQL](../../data/odbc/sql.md)\-Standardsyntax für den Zugriff auf die Daten eines DBMS.  
  
-   ODBC\-Treiber\-Manager  
  
     Eine Dynamic Link Library \(Odbc32.dll\), die für eine Anwendung ODBC\-Datenbanktreiber lädt.  Diese DLL ist für die Anwendung transparent.  
  
-   ODBC\-Datenbanktreiber  
  
     Eine oder mehrere DLLs, die ODBC\-Funktionsaufrufe für ein bestimmtes DBMS verarbeiten.  Eine Liste der zur Verfügung stehenden Treiber finden Sie unter [Liste der ODBC\-Treiber](../../data/odbc/odbc-driver-list.md).  
  
-   [ODBC\-Cursorbibliothek](../../data/odbc/odbc-the-odbc-cursor-library.md)  
  
     Eine Dynamic Link Library \(Odbccr32.dll\), die mit dem ODBC\-Treiber\-Manager und den Treibern zusammenwirkt und das Scrollen durch die Daten durchführt.  
  
-   [ODBC\-Administrator](../../data/odbc/odbc-administrator.md)  
  
     Ein Tool für die Konfiguration eines DBMS, um dieses als Datenquelle für eine Anwendung verfügbar zu machen.  
  
 Eine Anwendung erreicht die Unabhängigkeit von den Datenbank\-Management\-Systemen, indem sie, statt direkt mit dem DBMS zu arbeiten, mit einem ODBC\-Treiber arbeitet, der speziell für ein bestimmtes DBMS geschrieben wurde.  Der Treiber übersetzt die Aufrufe in Befehle, die das DBMS unterstützt. So vereinfacht sich die Arbeit des Entwicklers, und die Anwendung ist für eine große Bandbreite von Datenquellen geeignet.  
  
 Die Datenbankklassen unterstützen jede Datenquelle, für die ein ODBC\-Treiber zur Verfügung steht.  Dies könnte z. B. eine relationale Datenbank sein, eine ISAM \(Indexed Sequential Access Method\)\-Datenbank, ein Microsoft Excel\-Arbeitsblatt oder eine Textdatei.  Die ODBC\-Treiber verwalten die Verbindungen zur Datenquelle. Für die Auswahl von Datensätzen aus der Datenbank wird SQL verwendet.  
  
 Eine Liste der in dieser Version von Visual C\+\+ mitgelieferten ODBC\-Treiber sowie Informationen über den Erwerb zusätzlicher Treiber finden Sie unter [Liste der ODBC\-Treiber](../../data/odbc/odbc-driver-list.md).  
  
## Siehe auch  
 [Open Database Connectivity \(ODBC\)](../../data/odbc/open-database-connectivity-odbc.md)