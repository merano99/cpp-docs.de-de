---
title: "F&#252;r Visual&#160;C++-Projekte erstellte Dateitypen"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "Headerdateien [C++], Visual C++-Projekte"
  - "ActiveX-Steuerelemente [C++], Hilfedateien"
  - "DEF-Dateien"
  - "Projektelemente [C++], Dateien"
  - "Visual C++-Projekte, Dateien und Verzeichnissen"
  - "Ressourcendateien, vom Assistenten erstellte"
  - "Dateien [C++], Erweiterungen"
  - "Hilfedateien, für ActiveX-Steuerelemente"
  - "Webprojekte [C++], Hinzufügen von Elementen"
  - "DEF-Dateien"
  - "Lizenzieren von ActiveX-Steuerelementen"
ms.assetid: 2b0ee2e0-ae81-4185-9bb9-11da3c99a283
caps.latest.revision: 20
caps.handback.revision: "20"
ms.author: "mblome"
manager: "ghogen"
---
# F&#252;r Visual&#160;C++-Projekte erstellte Dateitypen
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

In diesem Thema werden alle mit Visual C\+\+\-Projekten für klassische Desktopcomputeranwendungen verknüpften Dateitypen beschrieben. Die in Ihrem Projekt tatsächlich enthaltenen Dateien sind vom Projekttyp und von Ihnen mithilfe eines Assistenten ausgewählten Optionen abhängig.  
  
-   [Projekt\- und Projektmappendateien](../ide/project-and-solution-files.md)  
  
-   [CLR\-Projekte](../ide/files-created-for-clr-projects.md)  
  
-   [ATL\-Programm oder Steuern von Quell\- und Headerdateien](../ide/atl-program-or-control-source-and-header-files.md)  
  
-   [MFC\-Programm oder Steuern von Quell\- und Headerdateien](../ide/mfc-program-or-control-source-and-header-files.md)  
  
-   [Vorkompilierte Headerdateien](../ide/precompiled-header-files.md)  
  
-   [Ressourcendateien](../ide/resource-files-cpp.md)  
  
-   [Hilfedateien \(WinHelp\)](../ide/help-files-winhelp.md)  
  
-   [Hinweisdateien](../ide/hint-files.md)  
  
 Beim [Erstellen eines Visual C\+\+\-Projekts](../ide/creating-desktop-projects-by-using-application-wizards.md) erstellen Sie möglicherweise eine neue Projektmappe, oder Sie fügen möglicherweise einer Projektmappe ein Projekt hinzu. Nicht triviale Anwendungen werden häufig mit mehreren Projekten in einer Projektmappe entwickelt.  
  
 Projekte generieren für gewöhnlich entweder eine EXE\- oder eine DLL\-Datei. Projekte können voneinander abhängig sein. Während des Buildprozesses nimmt die Visual C\+\+\-Umgebung Überprüfungen hinsichtlich Abhängigkeiten in und zwischen Projekten vor. Jedes Projekt verfügt über einen Hauptquellcode, und in Abhängigkeit der Projektart weist es möglicherweise viele andere Dateien auf, die verschieden Aspekte des Projekts enthalten. Die Inhalte dieser Dateien werden durch die Dateierweiterung angegeben. Die Visual Studio\-Entwicklungsumgebung verwendet die Dateierweiterungen, um zu bestimmen, wie die Dateiinhalte während eines Builds verarbeitet werden.  
  
 In der folgenden Tabelle werden allgemeine Dateien in einem Visual C\+\+\-Projekt mitsamt der zugehörigen Dateierweiterung gezeigt.  
  
|Dateierweiterung|Typ|Inhalt|  
|----------------------|---------|------------|  
|.asmx|Quelle|Bereitstellungsdatei.|  
|.asp|Quelle|Aktive Serverseitendatei|  
|.atp|Projekt|Anwendungsvorlagen\-Projektdatei.|  
|.bmp, .dib, .gif, .jpg, .jpeg, .png|Ressource|Allgemeine Bilddateien.|  
|.bsc|Kompilieren|Browsercodedatei.|  
|.cpp; .c|Quelle|Haupt\-Quellcodedateien für Ihre Anwendung.|  
|.cur|Ressource|Cursorbitmap\-Grafikdatei.|  
|.dbp|Projekt|Datenbankprojektdatei.|  
|.disco|Quelle|Dynamische Ermittlungsdokumentdatei. Verarbeitet die XML\-Webdienstermittlung.|  
|.exe, .dll|Projekt|Ausführbare oder Dynamic\-Link Library\-Dateien.|  
|H|Quelle|Headerdatei \(include\).|  
|.htm, .html, .xsp, .asp, .htc, .hta, .xml|Ressource|Allgemeine Webdateien.|  
|.HxC|Projekt|Hilfsprojektdatei.|  
|.ico|Ressource|Symbolbitmap\-Grafikdatei.|  
|.idb|Kompilieren|Die die Abhängigkeitsinformationen zwischen den Quelldateien und Klassendefinitionen enthaltende Statusdatei, die durch den Compiler während der minimalen Neuerstellung und der inkrementellen Kompilierung verwendet werden kann. Verwenden Sie die Compileroption [\/Fd](../build/reference/fd-program-database-file-name.md) zum Angeben des Namens der IDB\-Datei. Weitere Informationen finden Sie unter [\/Gm \(Minimale Neuerstellung aktivieren\)](../build/reference/gm-enable-minimal-rebuild.md).|  
|.idl|Kompilieren|Eine IDL\-Datei. Weitere Informationen finden Sie unter [Schnittstellendefinitionsdatei](http://msdn.microsoft.com/library/windows/desktop/aa378712) im [!INCLUDE[winsdkshort](../atl/reference/includes/winsdkshort_md.md)].|  
|.ilk|Verknüpfen|Datei für inkrementelle Verknüpfung. Weitere Informationen finden Sie unter [\/INCREMENTAL](../build/reference/incremental-link-incrementally.md).|  
|.map|Verknüpfen|Eine Textdatei mit Linkerinformationen. Verwenden Sie die Compileroption [\/Fm](../build/reference/fm-name-mapfile.md), um die MAP\-Datei zu benennen. Weitere Informationen finden Sie unter [\/MAP](../build/reference/map-generate-mapfile.md).|  
|.mfcribbon\-ms|Ressource|Eine den die Schaltflächen, Steuerelemente und Attribute im Menüband definierenden XML\-Code enthaltende Ressourcendatei. Weitere Informationen finden Sie unter [Menüband\-Designer \(MFC\)](../mfc/ribbon-designer-mfc.md).|  
|.obj, .o||Objektdateien, kompiliert, aber nicht verknüpft.|  
|.pch|Debug|Vorkompilierte Headerdatei.|  
|.rc, .rc2|Ressource|[Ressourcenskriptdateien](../mfc/working-with-resource-files.md) zum Generieren von Ressourcen.|  
|.sbr|Kompilieren|Zwischendatei des Quellbrowsers. Die Eingabedatei für [BSCMAKE](../build/reference/bscmake-options.md).|  
|.sln|Lösung|Die [Projektmappen](assetId:///a45c299d-69f5-4b67-879d-1383417df0a7)datei.|  
|.suo|Lösung|Die Datei mit den Projektmappenoptionen.|  
|.txt|Ressource|Eine Textdatei, in der Regel die Infodatei.|  
|.vap|Projekt|Eine Visual Studio Analyzer\-Projektdatei.|  
|.vbg|Lösung|Eine kompatible Projektgruppendatei.|  
|.vbp, .vip, .vbproj|Projekt|Die Visual Basic\-Projektdatei.|  
|.vcxproj|Projekt|Die Visual C\+\+\-Projektdatei. Weitere Informationen finden Sie unter [Projektdateien und Makefiles](../ide/project-and-solution-files.md).|  
|.vcxproj.filters|Projekt|Wenn der Projektmappen\-Explorer verwendet wird, um einem Projekt eine Datei hinzuzufügen, definiert die Filterdatei auf Grundlage der entsprechenden Dateinamenserweiterung, wo in der Projektmappen\-Explorer\-Gesamtstrukturansicht die Datei hinzugefügt wird.|  
|.vdproj|Projekt|Die Visual Studio\-Bereitstellungsprojektdatei.|  
|.vmx|Projekt|Die Makro\-Projektdatei.|  
|.vup|Projekt|Der Hilfsprogramm\-Projektdatei.|  
  
 Weitere Informationen über andere mit Visual Studio verknüpfte Dateien finden Sie unter [Dateitypen und Dateierweiterungen in Visual Studio .NET](../Topic/Project%20and%20Solution%20File%20Types.md).  
  
 Projektdateien sind in Ordnern im Projektmappen\-Explorer organisiert. Visual C\+\+ erstellt einen Ordner für Quelldateien, Headerdateien und Ressourcendateien. Sie können diese Ordner jedoch neu anordnen oder neue erstellen. Sie können Ordner verwenden, um logische Cluster von Dateien innerhalb der Hierarchie eines Projekts explizit zu organisieren. Beispielsweise können Sie Ordner so erstellen, dass sie alle Ihre Benutzeroberflächen\-Quelldateien oder Spezifikationen, Dokumentationen oder Testsammlungen enthalten. Alle Dateiordnernamen sollten eindeutig sein.  
  
 Wenn Sie einem Projekt ein Element hinzufügen, fügen Sie das Element zu allen Konfigurationen für dieses Projekt hinzu, unabhängig davon, ob das Element erstellt werden kann. Wenn Sie beispielsweise über ein Projekt mit dem Namen „MeinProjekt“ verfügen, wird das Element durch das Hinzufügen zu den Debug\- und Release\-Projektkonfigurationen hinzugefügt.  
  
## Siehe auch  
 [Erstellen und Verwalten von Visual C\+\+\-Projekten](../ide/creating-and-managing-visual-cpp-projects.md)   
 [Visual C\+\+\-Projekttypen](../ide/visual-cpp-project-types.md)   
 [Assistentenunterstützung für andere Sprachen](../ide/wizard-support-for-other-languages.md)