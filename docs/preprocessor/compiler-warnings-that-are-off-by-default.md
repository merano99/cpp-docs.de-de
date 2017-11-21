---
title: "Compiler-Warnungen, die standardmäßig deaktiviert sind | Microsoft Docs"
ms.date: 11/04/2016
ms.technology: cpp-tools
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- warnings, compiler
- cl.exe compiler, setting options
ms.assetid: 69809cfb-a38a-4035-b154-283a61938df8
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 1dec9728679629f25ddbea93956fd25d9b29ef59
ms.sourcegitcommit: 69632887f7a85f4841c49b4c1353d3144927a52c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2017
---
# <a name="compiler-warnings-that-are-off-by-default"></a>Standardmäßig deaktivierte Compilerwarnungen

Der Compiler schließt Warnungen ein, die standardmäßig deaktiviert sind, da die meisten Benutzer sieh nicht sehen möchten. Sie können jedoch diese Warnungen aktivieren, indem Sie eine der folgenden Optionen verwenden.

`#pragma warning(default : warning_number )`  
Die angegebene Warnung (`warning_number`) wird auf der Standardebene aktiviert. Dokumentation für die Warnung enthält die Standardebene der Warnung.

`#pragma warning( warning_level : warning_number )`  
Die angegebene Warnung (`warning_number`) wird auf der angegebenen Ebene (`warning_level`) aktiviert.

[/ Wall](../build/reference/compiler-option-warning-level.md)  
**/ Wall** aktiviert alle Warnungen, die standardmäßig deaktiviert sind.

Standardmäßig werden die folgenden Warnungen deaktiviert.

|||
|-|-|
|[C4061](../error-messages/compiler-warnings/compiler-warning-level-4-c4061.md) (Stufe 4)|Enumerator 'identifier' in einem Schalter der Enumeration 'enumeration' wird nicht explizit von einer case-Bezeichnung gehandhabt|
|[C4062](../error-messages/compiler-warnings/compiler-warning-level-4-c4062.md) (Stufe 4)|Enumerator 'identifier' in switch (enum) 'enumeration' wird nicht verarbeitet|
|C4191 (Ebene 3)|'operator/operation': unsichere Konvertierung von 'type of expression' zu 'type required'|
|[C4242](../error-messages/compiler-warnings/compiler-warning-level-4-c4242.md) (Stufe 4)|'identifier': Umwandlung von 'type1' in 'type2', Datenverlust ist möglich|
|[C4254](../error-messages/compiler-warnings/compiler-warning-level-4-c4254.md) (Stufe 4)|'operator': Umwandlung von 'type1' in 'type2', Datenverlust ist möglich|
|[C4255](../error-messages/compiler-warnings/compiler-warning-level-4-c4255.md) (Stufe 4)|'function': Kein Funktionsprototyp angegeben: '()' wird in '(void)' konvertiert|
|[C4263](../error-messages/compiler-warnings/compiler-warning-level-4-c4263.md) (Stufe 4)|'Funktion': Memberfunktion überschreibt keine virtuelle Memberfunktion einer Basisklasse|
|[C4264](../error-messages/compiler-warnings/compiler-warning-level-1-c4264.md) (Stufe 1)|'virtual_function': Keine Überschreibung für virtuelle Memberfunktion der Basis 'class' verfügbar; die Funktion wird ausgeblendet|
|[C4265](../error-messages/compiler-warnings/compiler-warning-level-3-c4265.md) (Stufe 3)|'Klasse': Die Klasse verfügt über virtuelle Funktionen, der Destruktor ist jedoch nicht virtuell|
|[C4266](../error-messages/compiler-warnings/compiler-warning-level-4-c4266.md) (Stufe 4)|'function': Keine Überschreibung für virtuelle Memberfunktion der Basis 'type' verfügbar; die Funktion wird ausgeblendet|
|[C4287](../error-messages/compiler-warnings/compiler-warning-level-3-c4287.md) (Stufe 3)|'Operator': Konflikt zwischen vorzeichenloser und negativer Konstante|
|[C4289](../error-messages/compiler-warnings/compiler-warning-level-4-c4289.md) (Stufe 4)|Nicht dem Standard entsprechende Erweiterung: 'var': Die loop-Steuerelementvariable, die in der for-Schleife deklariert wurde, wird außerhalb des for-Schleifenbereichs verwendet|
|[C4296](../error-messages/compiler-warnings/compiler-warning-level-4-c4296.md) (Stufe 4)|'Operator': der Ausdruck ist immer false|
|[C4339](../error-messages/compiler-warnings/compiler-warning-level-4-c4339.md) (Stufe 4)|'Typ' : Die Verwendung eines undefinierten Typs wurde in CLR-Metadaten entdeckt. Das Verwenden dieses Typs führt möglicherweise zu einer Laufzeitausnahme|
|[C4342](../error-messages/compiler-warnings/compiler-warning-level-1-c4342.md) (Stufe 1)|Verhaltensänderung: 'Funktion' wird aufgerufen, in früheren Versionen wurde jedoch ein Memberoperator aufgerufen.|
|[C4350](../error-messages/compiler-warnings/compiler-warning-level-1-c4350.md) (Stufe 1)|Verhaltensänderung: 'Member1' wird anstelle von 'Member2' aufgerufen|
|[C4355 GENERIERT](../error-messages/compiler-warnings/compiler-warning-c4355.md)|"this": Wird in der Basisliste für den Memberinitialisierer verwendet|
|[C4365](../error-messages/compiler-warnings/compiler-warning-level-4-c4365.md) (Stufe 4)|'action': Konvertierung von 'type_1' zu 'type_2', Konflikt zwischen 'signed' und 'unsigned'|
|C4370 (Stufe 3)|Durch bessere Verpackung wurde das Klassenlayout geändert, das vorher eine andere Compilerversion hatte|
|C4371 (Stufe 3)|Durch bessere Verpackung des Members 'member' wurde das Klassenlayout geändert, das vorher eine andere Compilerversion hatte|
|C4388 (Stufe 4)|Konflikt zwischen 'signed' und 'unsigned'|
|[C4412](../error-messages/compiler-warnings/compiler-warning-level-2-c4412.md) (Ebene 2)|'function': Funktionssignatur enthält Typ 'type'; C++-Objekte können nicht sicher zwischen reinem und gemischtem oder systemeigenem Code übergeben werden|
|C4426 (Stufe 1)|optimierungseinstellungen geändert, nachdem einschließlich Header, möglicherweise aufgrund von #pragma optimize()|
|[C4435](../error-messages/compiler-warnings/compiler-warning-level-4-c4435.md) (Stufe 4)|'class1' : Das Objektlayout unter „/vd2“ wird aufgrund der virtuellen Basis 'class2' geändert.|
|[C4437](../error-messages/compiler-warnings/compiler-warning-level-4-c4437.md) (Stufe 4)|dynamic_cast von virtueller Basis 'class1' zu 'class2' schlägt möglicherweise bei einigen Kontexten fehl|
|C4444 (Stufe 3)|Höchste Ebene '__unaligned' ist in diesem Kontext nicht implementiert|
|C4464 (Stufe 4)|Relative Includepfad enthält '..'|
|C4472 (Stufe 1)|'Bezeichner' ist eine systemeigene Enumeration: Fügen Sie einen Zugriffsspezifizierer (privat/öffentlich) hinzu, um eine verwaltete Enumeration zu deklarieren|
|[C4514](../error-messages/compiler-warnings/compiler-warning-level-4-c4514.md) (Stufe 4)|'Funktion': Nicht referenzierte Inlinefunktion wurde entfernt|
|[C4536](../error-messages/compiler-warnings/compiler-warning-level-4-c4536.md) (Stufe 4)|'type name': Der Typenname ist größer als das Metadatenlimit von 'limit'-Zeichen|
|[C4545](../error-messages/compiler-warnings/compiler-warning-level-1-c4545.md) (Stufe 1)|Ausdruck vor dem Komma wird als Funktion ausgewertet, der eine Argumentliste fehlt|
|[C4546](../error-messages/compiler-warnings/compiler-warning-level-1-c4546.md) (Stufe 1)|Funktionsaufruf vor dem Komma ohne Argumentliste|
|[C4547](../error-messages/compiler-warnings/compiler-warning-level-1-c4547.md) (Stufe 1)|'Operator': Operator vor dem Komma hat keine Auswirkungen; Operator mit Nebeneffekten erwartet|
|[C4548](../error-messages/compiler-warnings/compiler-warning-level-1-c4548.md) (Stufe 1)|Ausdruck vor dem Komma hat keine Auswirkung; es wurde ein Ausdruck mit Nebeneffekt erwartet|
|[C4549](../error-messages/compiler-warnings/compiler-warning-level-1-c4549.md) (Stufe 1)|'operator': Operator vor dem Komma hat keine Auswirkungen. War 'operator' beabsichtigt?|
|[C4555](../error-messages/compiler-warnings/compiler-warning-level-1-c4555.md) (Stufe 1)|Der Ausdruck hat keine Auswirkungen; Ausdruck mit Nebeneffekten erwartet|
|[C4557](../error-messages/compiler-warnings/compiler-warning-level-3-c4557.md) (Stufe 3)|'__assume' enthält den Effekt 'Effekt'|
|[C4571](../error-messages/compiler-warnings/compiler-warning-level-4-c4571.md) (Stufe 4)|Information: catch(...)-Semantik seit Visual C++ 7.1 geändert; strukturierte Ausnahmen (SEH) werden nicht mehr abgefangen.|
|C4574 (Stufe 4)|'identifier' wird als '0' definiert: beabsichtigten Sie, den '#if identifier' zu verwenden?|
|C4582 (Stufe 4)|"*Typ*': Konstruktor wird nicht implizit aufgerufen.|
|C4583 (Stufe 4)|"*Typ*": Destruktor wird nicht implizit aufgerufen.|
|C4587 (Stufe 1)|"*Anonymous_structure*": verhaltensänderung: Konstruktor wird nicht mehr implizit aufgerufen.|
|C4588 (Stufe 1)|"*Anonymous_structure*": verhaltensänderung: Destruktor wird nicht mehr implizit aufgerufen.|
|C4598 (Ebene 1 und Stufe 3)|' #include "*Header*" ": Anzahl der Header *Anzahl* im des vorkompilierten Headers stimmt nicht mit aktuellen Kompilierung an dieser Position|
|C4599 (Stufe 3)|"*Option* *Pfad*": Anzahl der Befehlszeilenargument *Anzahl* vorkompilierte Header stimmt nicht überein|
|C4605 (Stufe 1)|"/ D*Makro*" auf der aktuellen Befehlszeile durchführen angegeben, aber wurde nicht angegeben, wenn der vorkompilierter Header erstellt wurde|
|[C4619](../error-messages/compiler-warnings/compiler-warning-level-3-c4619.md) (Stufe 3)|#pragma-Warnung: Keine Warnungsnummer 'number' vorhanden|
|[C4623](../error-messages/compiler-warnings/compiler-warning-level-4-c4623.md) (Stufe 4)|'Abgeleitete Klasse': Der Standardkonstruktor konnte nicht generiert werden, da auf einen Basisklassen-Standardkonstruktor nicht zugegriffen werden kann|
|[C4625](../error-messages/compiler-warnings/compiler-warning-level-4-c4625.md) (Stufe 4)|'Abgeleitete Klasse': Der Kopierkonstruktor konnte nicht generiert werden, da auf einen Basisklassen-Kopierkonstruktor nicht zugegriffen werden kann|
|[C4626](../error-messages/compiler-warnings/compiler-warning-level-4-c4626.md) (Stufe 4)|'Abgeleitete Klasse': Der Zuweisungsoperator konnte nicht generiert werden, da auf einen Basisklassen-Zuweisungsoperator nicht zugegriffen werden kann|
|[C4628](../error-messages/compiler-warnings/compiler-warning-level-1-c4628.md) (Stufe 1)|'digraphs' werden mit '-Ze' nicht unterstützt. Die Zeichensequenz 'Digraph' wird nicht als alternativer Token für 'Zeichen' interpretiert.|
|[C4640](../error-messages/compiler-warnings/compiler-warning-level-3-c4640.md) (Stufe 3)|„Instanz“: Erstellen eines lokalen static-Objekts ist nicht threadsicher|
|C4647 (Stufe 3)|Verändertes Programmverhalten: __is_pod (*Typ*) anderen Wert aufweist, in früheren Versionen|
|C4654 (Stufe 4)|Code platziert werden, bevor der vorkompilierten Headerdatei umfassen Zeile werden ignoriert. Fügen Sie Code, um vorkompilierte Header.|
|[C4668](../error-messages/compiler-warnings/compiler-warning-level-4-c4668.md) (Stufe 4)|"*Symbol*'ist nicht definiert als ein Präprozessormakro, ersetzen durch '0' für'*Direktiven*"|
|C4682 (Stufe 4)|"*Symbol*': kein direktionales Parameterattribut angegeben, Standardwert [in]|
|[C4686](../error-messages/compiler-warnings/compiler-warning-level-3-c4686.md) (Stufe 3)|"*einen benutzerdefinierten Typ*': mögliche Änderung im Verhalten in der UDT gibt Aufrufkonvention zurück|
|[C4692](../error-messages/compiler-warnings/compiler-warning-level-1-c4692.md) (Stufe 1)|"*Funktion*": die Signatur des nicht privaten Members enthält den privaten systemeigenen Assemblytyp'systemeigener_Typ'|
|[C4710](../error-messages/compiler-warnings/compiler-warning-level-4-c4710.md) (Stufe 4)|"*Funktion*': Funktion nicht inline|
|[C4738](../error-messages/compiler-warnings/compiler-warning-level-3-c4738.md) (Stufe 3)|Das 32-Bit-Gleitkommaergebnis wird im Speicher gespeichert. Möglicherweise kommt es zu einem Leistungsverlust|
|[C4746](../error-messages/compiler-warnings/compiler-warning-c4746.md)|flüchtige Zugriff des "*Ausdruck*" / volatile des unterliegt:\<Iso &#124; ms > festlegen; in Betracht __iso_volatile_load/Store systeminterne Funktionen|
|C4749 (Stufe 4)|bedingt unterstützt: Offsetof auf non-standard-Layout-Typ angewendet "*Typ*"|
|C4767 (Stufe 4)|Name des Abschnitts "*Symbol*' ist länger als 8 Zeichen und wird vom Linker abgeschnitten|
|C4768 (Stufe 3)|__declspec-Attribute vor Verknüpfungsspezifikation werden ignoriert.|
|C4774 (Stufe 4)|"*Zeichenfolge*": im Argument erwartet Formatzeichenfolge *Anzahl* ist kein Zeichenfolgenliteral|
|C4786 (Stufe 3)|"*Symbol*': Objektname wurde auf 'Anzahl' Zeichen in den Debuginformationen gekürzt|
|[C4820](../error-messages/compiler-warnings/compiler-warning-level-4-c4820.md) (Stufe 4)|'Bytes' Bytes Abstand nach dem Konstrukt 'member_name'|
|C4826 (Ebene 2)|Konvertierung von '*Typ1*'to'*Typ2*' ist signaturerweitert. Dies kann zu unerwartetem Laufzeitverhalten führen.|
|C4837 (Stufe 4)|Trigraph erkannt: '?? *Zeichen*"ersetzt durch"*Zeichen*"|
|C4841 (Stufe 4)|nicht standardmäßige Erweiterung verwendet: zusammengesetzten Member-Kennzeichner in Offsetof verwendet|
|C4842 (Stufe 4)|Das Ergebnis des "Offsetof" auf einen Typ mit mehrfacher Vererbung angewendet wird nicht garantiert, Compilerversionen konsistent sein.|
|[C4868](../error-messages/compiler-warnings/compiler-warning-c4868.md) (Stufe 4)|"_Datei_(*Line_number*)" Compiler kann die Reihenfolge der Auswertung von links nach rechts in der Initialisierungsliste nicht erzwingen|
|[C4905](../error-messages/compiler-warnings/compiler-warning-level-1-c4905.md) (Stufe 1)|
          Breites Zeichenfolgenliteral umgewandelt zu "LPSTR"|
|[C4906](../error-messages/compiler-warnings/compiler-warning-level-1-c4906.md) (Stufe 1)|
          Zeichenfolgenliteral umgewandelt zu "LPWSTR"|
|[C4917](../error-messages/compiler-warnings/compiler-warning-level-1-c4917.md) (Stufe 1)|'Deklarator': Eine GUID kann nur mit einer Klasse, einer Schnittstelle oder einem Namespace verbunden werden|
|[C4928](../error-messages/compiler-warnings/compiler-warning-level-1-c4928.md) (Stufe 1)|Unzulässige Kopierinitialisierung. Mehrere benutzerdefinierte Konvertierungen wurden implizit übernommen|
|[C4931](../error-messages/compiler-warnings/compiler-warning-level-4-c4931.md) (Stufe 4)|Es wird angenommen, dass die Typbibliothek für Anzahl-Bit-Pointer erstellt wurde|
|[C4946](../error-messages/compiler-warnings/compiler-warning-level-1-c4946.md) (Stufe 1)|reinterpret_cast wird zwischen verknüpften Klassen verwendet: 'Klasse1' und 'Klasse2'|
|C4962|'Funktion': Profilgesteuerte Optimierungen wurden deaktiviert, da durch die Optimierungen eine Inkonsistenz zwischen den Profildaten verursacht wurde|
|[C4986](../error-messages/compiler-warnings/compiler-warning-c4986.md) (Stufe 4)|"*Symbol*': Ausnahmespezifikation stimmt nicht mit der vorherigen Deklaration überein|
|C4987 (Stufe 4)|Es wurde eine nicht standardmäßige Erweiterung verwendet: 'throw (...)'|
|C4988 (Stufe 4)|"*Symbol*': Variable deklariert Bereichs der äußeren Klasse/Funktion|
|C5022|"*Typ*': mehrere bewegungskonstruktoren angegeben|
|C5023|"*Typ*': mehrere Verschiebe-standardzuweisungsoperatoren angegeben|
|C5024 (Stufe 4)|"*Typ*": Verschieben Konstruktor wurde implizit als gelöscht definiert.|
|C5025 (Stufe 4)|"*Typ*': Zuweisungsoperator wurde implizit als gelöscht definiert, verschieben|
|C5026 (Ebene 1 und Stufe 4)|"*Typ*": Verschieben Konstruktor wurde implizit als gelöscht definiert.|
|C5027 (Ebene 1 und Stufe 4)|"*Typ*': Zuweisungsoperator wurde implizit als gelöscht definiert, verschieben|
|C5029 (Stufe 4)|nicht dem Standard entsprechende Erweiterung: Ausrichtungsattribute in C++, Zuweisen von Variablen, Datenmember und Transpondertypen nur|
|C5031 (Stufe 4)|#pragma warning"(POP): wahrscheinlich Konflikt die Folge, herunternehmen Status" Warnung "in anderen Datei abgelegt|
|C5032 (Stufe 4)|#pragma warning"(Push) ohne entsprechende #pragma warning"(POP) erkannt|
|C5035|Verwenden der Funktion "*Feature*" bewirkt, dass Funktion *Funktion* als Gast-Code kompiliert werden|
|C5036 (Stufe 1)|Beim Kompilieren mit /hybrid:x86arm64-Funktion Varargs zeigerkonvertierung "*Typ1*'to'*Typ2*"|

Diese Warnungen sind deaktiviert, es sei denn, die [/ liberalen-](../build/reference/permissive-standards-conformance.md) (Compileroption) festgelegt ist:

|||
|-|-|
|[C4471 (Stufe 4)](../error-messages/compiler-warnings/compiler-warning-level-4-c4471.md)|Für eine Vorwärtsdeklaration einer Enumeration ohne Bereichseinschränkung ist ein zugrunde liegender Typ erforderlich (int wird angenommen).|
|[C4608 (Stufe 3)](../error-messages/compiler-warnings/compiler-warning-level-3-c4608.md)|"Union\_Member' wurde bereits von einem anderen union-Member in der Initialisiererliste"Union_member"initialisiert wurde|


Diese Warnungen wurden deaktiviert standardmäßig in der Compiler vor Visual Studio 2015-Versionen:

|||
|-|-|
|[C4302](../error-messages/compiler-warnings/compiler-warning-level-2-c4302.md) (Ebene 2)|'conversion': Verkürzung von 'type1' in 'type2'|
|[C4311](../error-messages/compiler-warnings/compiler-warning-level-1-c4311.md) (Stufe 1)|'Variable': Zeigerverkürzung von 'Typ' zu 'Typ'|
|[C4312](../error-messages/compiler-warnings/compiler-warning-level-1-c4312.md) (Stufe 1)|'Operation': Konvertierung von 'Typ1' in größeren Typ 'Typ2'|
|[C4319](../error-messages/compiler-warnings/compiler-warning-level-1-c4319.md) (Stufe 1)|'Operator': 0 (null) Erweitern von "Typ1" in "Typ2" größerem|

Diese Warnungen wurden deaktiviert standardmäßig in der Compiler vor Visual Studio 2012-Versionen:

|||
|-|-|
|[C4431](../error-messages/compiler-warnings/compiler-warning-level-4-c4431.md) (Stufe 4)|Fehlender Typspezifizierer - int wird angenommen. Hinweis: default-int wird von C++ nicht unterstützt|

## <a name="see-also"></a>Siehe auch

[warning](../preprocessor/warning.md)