---
title: C/C++-Eigenschaften (Linux C++) | Microsoft Docs
ms.custom: 
ms.date: 9/26/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 4bb8894b-c874-4a68-935e-b127d54e484f
author: mikeblome
ms.author: mblome
manager: ghogen
f1_keywords:
- VC.Project.VCClangCompilerTool.AdditionalIncludeDirectories
- VC.Project.VCClangCompilerTool.DebugInformationFormat
- VC.Project.VCClangCompilerTool.ObjectFile
- VC.Project.VCClangCompilerTool.WarningLevel
- VC.Project.VCClangCompilerTool.WarnAsError
- VC.Project.VCClangCompilerTool.AdditionalWarning
- VC.Project.VCClangCompilerTool.Verbose
- VC.Project.VCConfiguration.BuildLogFile
- VC.Project.VCClangCompilerTool.Optimization
- VC.Project.VCClangCompilerTool.StrictAliasing
- VC.Project.VCClangCompilerTool.UnrollLoops
- VC.Project.VCClangCompilerTool.LinkTimeOptimization
- VC.Project.VCClangCompilerTool.OmitFramePointers
- VC.Project.VCClangCompilerTool.NoCommonBlocks
- VC.Project.VCClangCompilerTool.PIC
- VC.Project.VCClangCompilerTool.ThreadSafeStatics
- VC.Project.VCClangCompilerTool.RelaxIEEE
- VC.Project.VCClangCompilerTool.HideInlineMethods
- VC.Project.VCClangCompilerTool.SymbolsHiddenByDefault
- VC.Project.VCClangCompilerTool.ExceptionHandling
- VC.Project.VCClangCompilerTool.RuntimeTypeInfo
- VC.Project.VCClangCompilerTool.CLanguageStandard
- VC.Project.VCClangCompilerTool.CppLanguageStandard
- VC.Project.VCClangCompilerTool.PreprocessorDefinitions
- VC.Project.VCClangCompilerTool.UndefinePreprocessorDefinitions
- VC.Project.VCClangCompilerTool.UndefineAllPreprocessorDefinitions
- VC.Project.VCClangCompilerTool.ShowIncludes
- VC.Project.VCClangCompilerTool.CompileAs
- VC.Project.VCClangCompilerTool.ForcedIncludeFiles
- vc.project.AdditionalOptionsPage
ms.openlocfilehash: 94a22843c15e537a7af8e1e44827f8c1ab365165
ms.sourcegitcommit: ca2f94dfd015e0098a6eaf5c793ec532f1c97de1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2017
---
# <a name="cc-properties-linux-c"></a>C/C++-Eigenschaften (Linux C++)

## <a name="general"></a>Allgemein
Eigenschaft | Beschreibung | Auswahlmöglichkeiten
--- | ---| ---
Zusätzliche Includeverzeichnisse | Gibt mindestens ein Verzeichnis an, das dem include-Pfad hinzugefügt werden soll. Verwenden Sie Semikolons als Trennzeichen, wenn mehrere Verzeichnisse vorhanden sind. (-I[path]).
Debuginformationenformat | Gibt den Typ der Debuginformationen an, die vom Compiler generiert werden. | **Keine**: Generiert keine Debuginformationen, sodass die Kompilierung ggf. schneller erfolgt.<br>**Minimale Debuginformationen**: Generiert minimale Debuginformationen.<br>**Vollständige Debuginformationen (DWARF2)**: Generiert DWARF2-Debuginformationen.<br>
Name der Objektdatei | Gibt einen Namen an, um den Standardnamen der Objektdatei zu überschreiben. Dies kann ein Datei- oder Verzeichnisname sein. (-o [name]).
Warnstufe | Wählen Sie aus, wie streng der Compiler bei Codefehlern sein soll.  Andere Kennzeichnungen sollten direkt zu den zusätzlichen Optionen hinzugefügt werden. (/w, /Weverything). | **Alle Warnungen deaktivieren**: Deaktiviert alle Compilerwarnungen.<br>**EnableAllWarnings**: Aktiviert alle Warnungen, einschließlich standardmäßig deaktivierter Warnungen.<br>
Warnungen als Fehler behandeln | Behandelt alle Compilerwarnungen als Fehler. Für ein neues Projekt kann es empfehlenswert sein, /Werror in allen Kompilierungen zu verwenden. Das Auflösen aller Warnungen stellt sicher, dass die geringstmögliche Anzahl schwer zu findender Codefehler vorhanden ist.
Zusätzliche Warnungen für C | Definiert eine Sammlung zusätzlicher Warnmeldungen.
Zusätzliche Warnungen für C++ | Definiert eine Sammlung zusätzlicher Warnmeldungen.
Ausführlichen Modus aktivieren | Wenn der ausführliche Modus aktiviert ist, würde dieses Tool mehr Informationen ausgeben als bei der Diagnose des Builds.
C-Compiler | Gibt das Programm an, das beim Kompilieren von C-Quelldateien aufgerufen werden soll, oder den Pfad zum C-Compiler auf dem Remotesystem.
C++-Compiler | Gibt das Programm an, das beim Kompilieren von C++-Quelldateien aufgerufen werden soll, oder den Pfad zum C-Compiler auf dem Remotesystem.
Kompilierungstimeout | Das Remotekompilierungstimeout in Millisekunden.
Objektdateien kopieren | Gibt an, ob die kompilierten Objektdateien vom Remotesystem auf den lokalen Computer kopiert werden sollen.

## <a name="optimization"></a>Optimierung
Eigenschaft | Beschreibung | Auswahlmöglichkeiten
--- | ---| ---
Optimierung | Gibt die Optimierungsstufe für die Anwendung an. | **Benutzerdefiniert**: Benutzerdefinierte Optimierung.<br>**Deaktiviert**: Deaktivieren der Optimierung.<br>**Größe minimieren**: Größenoptimierung.<br>**Geschwindigkeit maximieren**: Geschwindigkeitsoptimierung.<br>**Vollständige Optimierung**: Teure Optimierungen.<br>
Strenges Aliasing | Annehmen der strengsten Aliasingregeln.  Bei einem Objekt eines Typs wird niemals davon ausgegangen, dass es sich an derselben Adresse befindet wie ein Objekt eines anderen Typs.
Schleifen auflösen | Lösen Sie Schleifen auf, um Anwendungen schneller zu machen, indem Sie die Anzahl der ausgeführten Branches verringern (auf Kosten einer größeren Codegröße).
Linkzeitoptimierung | Aktivieren Sie Optimierungen zwischen Prozeduren, indem Sie dem Optimierer die Möglichkeit geben, Objektdateien in Ihrer Anwendung zu durchsuchen.
Framezeiger unterdrücken | Unterdrückt die Erstellung von Framezeigern im Aufrufstapel.
Keine allgemeinen Textblöcke | Zuweisen auch nicht initialisierter globaler Variablen im Datenabschnitt der Objektdatei, anstatt sie als allgemeine Blöcke zu generieren

## <a name="preprocessor"></a>Präprozessor
Eigenschaft | Beschreibung | Auswahlmöglichkeiten
--- | ---| ---
Präprozessordefinitionen | Definiert Präprozessorsymbole für Ihre Quelldatei. (-D)
Präprozessordefinitionen aufheben | Gibt mindestens eine aufgehobene Präprozessordefinition an.  (-U [Makro])
Alle Präprozessordefinitionen aufheben | Hebt die Definition aller zuvor definierten Präprozessorwerte auf.  (-undef)
Includedateien anzeigen | Generiert eine Liste der Includedateien mit Compilerausgabe.  (-H)

## <a name="code-generation"></a>Codeerzeugung
Eigenschaft | Beschreibung | Auswahlmöglichkeiten
--- | ---| ---
Positionsunabhängiger Code | Generieren von positionsunabhängigem Code (Position Independent Code, PIC) für die Verwendung in einer freigegebenen Bibliothek.
Statische Elemente sind threadsicher | Aufgeben von Extra-Code, um in C++ ABI angegebene Routinen zur threadsicheren Initialisierung lokaler statischer Elemente zu verwenden. | **Nein**: Deaktivieren threadsicherer statischer Elemente.<br>**Ja**: Aktivieren threadsicherer statischer Elemente.<br>
Gleitkommaoptimierung | Ermöglicht Gleitkommaoptimierungen durch die Lockerung der IEEE-754-Konformität.
Inlinemethoden ausgeblendet | Wenn aktiviert, werden Out-of-Line-Kopien von Inlinemethoden als „private extern“ deklariert.
Symbole standardmäßig ausgeblendet | Alle Symbole werden als „private extern“ deklariert, es sei denn, sie sind explizit für den Export mit dem __attribute-Makro markiert.
C++-Ausnahmen aktivieren | Gibt das Ausnahmebehandlungsmodell an, das vom Compiler verwendet wird. | **Nein**: Ausnahmenbehandlung deaktivieren.<br>**Ja**:-Ausnahmebehandlung aktivieren.<br>

## <a name="language"></a>Sprache
Eigenschaft | Beschreibung | Auswahlmöglichkeiten
--- | ---| ---
Laufzeit-Typeninformation aktivieren | Fügt Code für die Überprüfung der C++-Objekttypen während der Laufzeit hinzu (Laufzeit-Typinformationen).     (frtti, fno-rtti)
C-Sprachstandard | Bestimmt den C-Sprachstandard. | **Default**<br>**C89**: C89-Sprachstandard.<br>**C99**: C99-Sprachstandard.<br>**C11**: C11-Sprachstandard.<br>**C99 (GNU-Dialekt)**: C99-Sprachstandard (GNU-Dialekt).<br>**C11 (GNU-Dialekt)**: C11-Sprachstandard (GNU-Dialekt).<br>
C++-Sprachstandard | Bestimmt den C++-Sprachstandard. | **Default**<br>**C++03**: C++03-Sprachstandard.<br>**C++11**: C++11-Sprachstandard.<br>**C++14**: C++14-Sprachstandard.<br>**C++03 (GNU-Dialekt)**: C++03-Sprachstandard (GNU-Dialekt).<br>**C++11 (GNU-Dialekt)**: C++11-Sprachstandard (GNU-Dialekt).<br>**C++14 (GNU-Dialekt)**: C++14-Sprachstandard (GNU-Dialekt).<br>

## <a name="advanced"></a>Erweitert
Eigenschaft | Beschreibung | Auswahlmöglichkeiten
--- | ---| ---
Kompilieren als | Auswählen der Kompilierungssprachenoption für C- und CPP-Dateien.  „Standard“ führt die Erkennung basierend auf der .c- oder .cpp-Dateierweiterung aus. (-x c, -x c++) | **Standard**: Die Standardeinstellung.<br>**Als C-Code kompilieren**: Kompilieren als C-Code.<br>**Als C++-Code kompilieren**: Kompilieren als C++-Code.<br>
Erzwungene Includedateien | Mindestens eine erzwungene Includedatei (-include [name])

## <a name="additional-options"></a>Zusätzliche Optionen 