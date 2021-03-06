---
title: / fp (Gleitkommaverhalten festlegen)
ms.date: 11/09/2018
f1_keywords:
- VC.Project.VCCLCompilerTool.floatingPointModel
- VC.Project.VCCLWCECompilerTool.FloatingPointExceptions
- /fp
- VC.Project.VCCLWCECompilerTool.floatingPointModel
- VC.Project.VCCLCompilerTool.FloatingPointExceptions
helpviewer_keywords:
- -fp compiler option [C++]
- /fp compiler option [C++]
ms.assetid: 10469d6b-e68b-4268-8075-d073f4f5d57e
ms.openlocfilehash: c571bf104fd7e8f6a287c3dd35c444d904b4b7e8
ms.sourcegitcommit: c85c8a1226d8fbbaa29f4691ed719f8e6cc6575c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2019
ms.locfileid: "54894093"
---
# <a name="fp-specify-floating-point-behavior"></a>/ fp (Gleitkommaverhalten festlegen)

Gibt an, wie der Compiler Gleitkommaausdrücken, Optimierungen und Ausnahmen behandelt. Die **/fp** Optionen angeben, ob der generierte Code ermöglicht gleitkommaumgebung ändert den Rundungsmodus des Gleitkommas Ausnahme Masken und subnormal Verhalten und gleitkommastatus überprüft, ob zurückgeben, aktuelle, genaue Ergebnisse. Es steuert, ob der Compiler Code generiert, die verwaltet Quellvorgang und die Reihenfolge des Ausdrucks entspricht dem Standard für die Weitergabe von NaN oder wenn es stattdessen effizienteren Code generiert, die möglicherweise neu anordnen oder Vorgänge zu kombinieren und vereinfachen algebraische Transformationen, die nicht im Standard zulässig sind.

## <a name="syntax"></a>Syntax

> **/fp:**[**precise** | **strict** | **fast** | **except**[**-**]]

### <a name="arguments"></a>Argumente

#### <a name="precise"></a>Präzise

Standardmäßig verwendet der Compiler **/fp: präzise** Verhalten.

Klicken Sie unter **/fp: präzise** der Compiler behält der Quellausdruck Sortier- und Eigenschaften der gleitkommacode Rundens, wenn es sich bei generiert und optimiert die Objektcode für den Zielcomputer. Der Compiler Rundet auf die Genauigkeit Code an vier bestimmten Punkten während der Auswertung von Ausdrücken: typenumwandlungen auf Zuweisungen an, wird von einem Funktionsaufruf ein gleitkommaarguments auf ein Funktionsaufruf übergeben wird und der Wert einer Gleitkommazahl zurückgegeben. Intermediate Berechnungen können auf Computer mit einfacher Genauigkeit ausgeführt werden. Typenumwandlungen können verwendet werden, um explizit zwischen Berechnungen zu runden.

Der Compiler führt keine algebraische Transformationen auf Gleitkommaausdrücken, z. B. neuzuordnung oder Verteilung, es sei denn, die Transformation eine bitweise identischen Ergebnis garantiert ist.
Gemäß IEEE-754-Spezifikationen werden die Ausdrücke für die spezielle Werte (NaN, + unendlich, – unendlich,-0.0) verarbeitet. Z. B. `x != x` ergibt **"true"** Wenn X gleich NaN ist. Gleitkomma *Kontraktionen*, d. h. computeranweisungen, die Operationen mit Gleitkommazahlen, kombinieren wird generiert, die unter **/fp: präzise**.

Der Compiler generiert Code für die Ausführung im vorgesehen der [Gleitkomma standardumgebung](#the-default-floating-point-environment) und setzt voraus, dass die gleitkommaumgebung nicht zugegriffen oder zur Laufzeit geändert wird. Das heißt, nimmt es, dass der Code nicht durch Aufheben der Maskierung Gleitkommaausnahmen, lesen oder gleitkommastatus registriert schreiben oder Rundungsmodi zu ändern.

Wenn Ihr gleitkommacode nicht der Reihenfolge der Operationen und Ausdrücke in den Gleitkomma-Anweisungen abhängt (beispielsweise, wenn es nicht relevant ist, ob `a * b + a * c` wird berechnet als `(b + c) * a` oder `2 * a` als `a + a`), sollten Sie die [fast](#fast) auswählen, um die schnellere und effizientere Code erstellt werden kann. Wenn Ihr Code sowohl hängt von der Reihenfolge der Operationen und Ausdrücke, und greift auf oder die gleitkommaumgebung (z. B. ändert um Rundungsmodi zu ändern oder zum Abfangen von Ausnahmen), verwenden [/fp: strict](#strict).

#### <a name="strict"></a>strict

**/ fp: strict** verhält sich ähnlich wie **/fp: präzise**, das heißt, der Compiler behält die Reihenfolge und Rundung Eigenschaften der gleitkommacode generiert und optimiert die Objektcode für den Zielcomputer , und den Standard beobachtet, bei der Behandlung der speziellen Werte. Das Programm kann darüber hinaus sicher zugreifen oder die gleitkommaumgebung zur Laufzeit ändern.

Klicken Sie unter **/fp: strict**, generiert der Compiler Code, der die Anwendung problemlos durch Aufheben der Maskierung Gleitkommaausnahmen, lesen oder Schreiben gleitkommastatus registriert, oder ändern Rundungsmodi ermöglicht. Es Rundet auf die Genauigkeit Code an vier bestimmten Punkten während der Auswertung von Ausdrücken: typenumwandlungen auf Zuweisungen an, wird von einem Funktionsaufruf ein gleitkommaarguments auf ein Funktionsaufruf übergeben wird und der Wert einer Gleitkommazahl zurückgegeben. Intermediate Berechnungen können auf Computer mit einfacher Genauigkeit ausgeführt werden. Typenumwandlungen können verwendet werden, um explizit zwischen Berechnungen zu runden. Der Compiler führt keine algebraische Transformationen auf Gleitkommaausdrücken, z. B. neuzuordnung oder Verteilung, es sei denn, die Transformation eine bitweise identischen Ergebnis garantiert ist. Gemäß IEEE-754-Spezifikationen werden die Ausdrücke für die spezielle Werte (NaN, + unendlich, – unendlich,-0.0) verarbeitet. Z. B. `x != x` ergibt **"true"** Wenn X gleich NaN ist. Gleitkomma Kontraktionen sind nicht unter generiert **/fp: strict**.

**/ fp: strict** ist dieses Verfahren teurer als **/fp: präzise** , da der Compiler zusätzliche Anweisungen zum Abfangen von Ausnahmen und zulassen, dass Programme zugreifen oder diese ändern der gleitkommaumgebung an einfügen muss Common Language Runtime. Wenn Code dieser Funktion nicht verwenden, jedoch erfordern Code Reihenfolge und runden oder auf speziellen Werte basiert, verwenden Sie **/fp: präzise**. Andernfalls in Betracht **fast**, die zu der schneller und kürzer Code führen können.

#### <a name="fast"></a>Schnelle

Die **fast** Option ermöglicht dem Compiler, neu anordnen, kombinieren und vereinfachen von Gleitkommaoperationen um gleitkommacode für Geschwindigkeit und den Speicherplatz zu optimieren. Der Compiler möglicherweise weglassen Rundung am zuweisungsanweisungen, typenumwandlungen oder Funktionsaufrufe. Es kann neu anordnen Vorgänge oder durchführen algebraische Transformationen, z. B. durch Verwendung von assoziative und distributive Gesetze, auch wenn diese Transformationen zu Funktionsmember verschiedene Rundungsverhalten führen. Dank dieser erweiterten Optimierung, das Ergebnis des einige gleitkommaberechnungen unterscheiden sich möglicherweise von solchen, die in anderen **/fp** Optionen. Spezielle Werte (NaN, + unendlich, – unendlich,-0.0) möglicherweise nicht weitergegeben werden, oder Verhalten sich genau entsprechend dem IEEE-754-Standard. Gleitkomma Kontraktionen werden generiert, die unter **fast**. Der Compiler ist noch gebunden, von der zugrunde liegenden Architektur unter **fast**, und weitere Optimierungen zur Verfügung, durch die Verwendung von der [/arch](../../build/reference/arch-minimum-cpu-architecture.md) Option.

Klicken Sie unter **fast**, der Compiler generiert Code für die direkte Verwendung in der Standard-Gleitkomma-Umgebung ausgeführt und wird davon ausgegangen, dass die gleitkommaumgebung nicht zugegriffen oder zur Laufzeit geändert werden. Das heißt, nimmt es, dass der Code nicht durch Aufheben der Maskierung Gleitkommaausnahmen, lesen oder gleitkommastatus registriert schreiben oder Rundungsmodi zu ändern.

**fast** ist für Programme, erfordern keine strict Source Code Sortierung und Runden von Gleitkomma-Ausdrücke, und verlassen Sie sich nicht auf den Standardregeln für den Umgang mit spezieller Werten wie z. B. NaN, vorgesehen. Wenn Ihr gleitkommacode auf dem Standardverhalten der speziellen Werte, die verwendet basiert oder Beibehaltung des Quellcodes benötigt, Sortierung und Runden von [/fp: präzise](#precise). Wenn Ihr Code greift auf oder die gleitkommaumgebung ändert um Rundungsmodi zu ändern, Aufheben der Maskierung Gleitkommaausnahmen wird oder Gleitkomma-Status überprüfen, verwenden Sie [/fp: strict](#strict).

#### <a name="except"></a>Mit der Ausnahme

Die **/fp: mit Ausnahme von** Option generiert Code, um sicherzustellen, dass ohne Maskierung Gleitkommaausnahmen werden ausgelöst, auf den genauen Punkt, an dem sie auftreten, und keine zusätzlichen Gleitkommaausnahmen ausgelöst werden. In der Standardeinstellung die **/fp: strict** -Option aktiviert **/fp: mit Ausnahme von**, und **/fp: präzise** nicht. Die **/fp: mit Ausnahme von** Option ist nicht kompatibel mit **fast**. Die Option kann explizit deaktiviert werden, indem wir **/fp: mit Ausnahme von-**.

Beachten Sie, dass **/fp: mit Ausnahme von** aktiviert Gleitkommaausnahmen nicht von selbst, dies ist jedoch erforderlich für Programme, um Gleitkommaausnahmen zu aktivieren. Finden Sie unter [_controlfp](../../c-runtime-library/reference/control87-controlfp-control87-2.md) Informationen zur Aktivierung von Gleitkommaausnahmen.

## <a name="remarks"></a>Hinweise

Mehrere **/fp** -Optionen können in der gleichen Compiler-Befehlszeile angegeben werden. Nur einer der **/fp: strict**, **fast**, und **/fp: präzise** Optionen können zu einem Zeitpunkt gültig sein. Wenn mehr als eine der folgenden Optionen in der Befehlszeile angegeben wird, die höhere Option hat Vorrang vor, und der Compiler generiert eine Warnung. Die **/fp: strict** und **/fp: mit Ausnahme von** Optionen sind nicht kompatibel mit **"/ CLR"**.

Die [/Za](../../build/reference/za-ze-disable-language-extensions.md) (ANSI-Kompatibilität) Option ist nicht kompatibel mit **/fp**.

### <a name="using-pragmas-to-control-floating-point-behavior"></a>Mithilfe des Pragmas Steuerelement Gleitkomma-Verhalten

Der Compiler bietet drei Pragma-Direktiven überschreiben die Gleitkommaverhalten in der Befehlszeile angegeben: [Float_control](../../preprocessor/float-control.md), [Fenv_access](../../preprocessor/fenv-access.md), und [Fp_contract](../../preprocessor/fp-contract.md). Sie können diese Pragmas verwenden, zum Steuern des Gleitkommaverhaltens auf Funktionsebene, nicht innerhalb einer Funktion. Beachten Sie, dass diese Pragmas nicht direkt entsprechen den **/fp** Optionen. Diese Tabelle zeigt, wie die **/fp** Optionen und Pragmas zugeordnet werden, miteinander. Weitere Informationen finden Sie in der Dokumentation für die einzelnen Optionen und Pragmas.

||float_control(precise)|float_control(except)|fenv_access|fp_contract|
|-|-|-|-|-|
|**/fp:fast**|Ausschalten|Ausschalten|Ausschalten|an|
|**/fp:precise**|an|Ausschalten|Ausschalten|an|
|**/fp:strict**|an|an|an|Ausschalten|

### <a name="the-default-floating-point-environment"></a>Die standardumgebung floating point

Wenn ein Prozess initialisiert wird, die *Standard floating-Point-Umgebung* festgelegt ist. Diese Umgebung alle Gleitkommaausnahmen maskiert, legt den Rundungsmodus, auf die gerundet nächste (`FE_TONEAREST`), behält subnormal (denormal) Werte, die standardgenauigkeit der Mantisse (Mantisse) verwendet, für die **"float"**, **doppelte**, und **long double** Werte ein, und wenn dies unterstützt wird, wird das Steuerelement unendlich affine Standardmodus.

### <a name="floating-point-environment-access-and-modification"></a>Gleitkommaumgebung und Änderungszeiten

Die Microsoft Visual C++-Laufzeit stellt mehrere Funktionen zum Zugreifen auf und ändern die gleitkommaumgebung bereit. Dazu gehören [_controlfp](../../c-runtime-library/reference/control87-controlfp-control87-2.md), [_clearfp](../../c-runtime-library/reference/clear87-clearfp.md), und [_statusfp](../../c-runtime-library/reference/status87-statusfp-statusfp2.md) und deren Varianten. Um korrekte Verhalten sicherzustellen, dass wenn Ihr Code greift auf oder die gleitkommaumgebung ändert, `fenv_access` muss aktiviert sein, entweder durch die **/fp: strict** aus oder durch die Verwendung eines der `fenv_access` Pragma für diese Funktionen haben Sie keine Auswirkung. Wenn `fenv_access` ist nicht aktiviert ist, Zugriff oder Änderung von die gleitkommaumgebung möglicherweise unerwartete Programmverhalten: Code kann die angeforderte Änderungen an die gleitkommaumgebung nicht berücksichtigt, die Register gleitkommastatus melden möglicherweise nicht erwartete oder aktuelle Ergebnisse und unerwartete Ausnahmen auftreten, oder erwarteten Gleitkommaausnahmen nicht auftreten.

Wenn Ihr Code greift auf oder die gleitkommaumgebung ändert, achten Sie beim Kombinieren von Code, in denen `fenv_access` aktiviert ist, durch Code, der keine `fenv_access` aktiviert. Im Code, in denen `fenv_access` nicht aktiviert ist, wird der Compiler davon aus, die die gleitkommaumgebung für die Plattform standardmäßig aktiviert ist, und, die der gleitkommastatus nicht zugegriffen oder geändert wird. Es wird empfohlen, Sie speichern und die lokale gleitkommaumgebung in den Standardzustand wiederherstellen, bevor die Steuerung an eine Funktion übertragen wird, die nicht `fenv_access` aktiviert. In diesem Beispiel wird veranschaulicht, wie die `float_control` Pragma eingerichtet und wiederhergestellt werden kann:

```cpp
#pragma float_control(strict, on, push)
// Code that uses /fp:strict mode
#pragma float_control(pop)
```

### <a name="floating-point-rounding-modes"></a>Gleitkomma Rundungsmodi zur Verfügung

In beiden Verzeichnissen **/fp: präzise** und **fast** der Compiler generiert Code für die direkte Verwendung in der Standard-Gleitkomma-Umgebung ausgeführt und wird davon ausgegangen, dass die Umgebung nicht zugegriffen oder zur Laufzeit geändert werden. Das heißt, nimmt es, dass der Code nicht durch Aufheben der Maskierung Gleitkommaausnahmen, lesen oder gleitkommastatus registriert schreiben oder Rundungsmodi zu ändern.  Allerdings müssen einige Programme, die gleitkommaumgebung zu ändern. Beispielsweise berechnet in diesem Beispiel Fehlergrenzen ein Gleitkomma Multiplikation durch Ändern von Gleitkomma Rundungsmodi zur Verfügung:

```cpp
// fp_error_bounds.cpp
#include <iostream>
#include <limits>
using namespace std;

int main(void)
{
    float a = std::<float>::max();
    float b = -1.1;
    float cLower = 0.0;
    float cUpper = 0.0;
    unsigned int control_word = 0;
    int err = 0;

    // compute lower error bound.
    // set rounding mode to -infinity.
    err = _controlfp_s(&control_word, _RC_DOWN, _MCW_RC);
    if (err)
    {
        cout << "_controlfp_s(&control_word, _RC_DOWN, _MCW_RC) failed with error:" << err << endl;
    }  
    cLower = a * b;

    // compute upper error bound.
    // set rounding mode to +infinity.
    err = _controlfp_s(&control_word, _RC_UP, _MCW_RC);
    if (err)
    {
        cout << "_controlfp_s(&control_word, _RC_UP, _MCW_RC) failed with error:" << err << endl;
    }
    cUpper = a * b;

    // restore default rounding mode.
    err = _controlfp_s(&control_word, _CW_DEFAULT, _MCW_RC);
    if (err)
    {
        cout << "_controlfp_s(&control_word, _CW_DEFAULT, _MCW_RC) failed with error:" << err << endl;
    }
    // display error bounds.
    cout << "cLower = " << cLower << endl;
    cout << "cUpper = " << cUpper << endl;
    return 0;
}
```

Da nimmt der Compiler die standardmäßigen floating-Point-Umgebung unter **fast** und **/fp: präzise** ist kostenlos, um die Aufrufe an ignorieren `_controlfp_s`. Beispielsweise wird beim Kompilieren mit sowohl **"/ O2"** und **/fp: präzise** für die X86 Architektur, das die Begrenzungen nicht berechnet werden und gibt das Beispielprogramm:

```Output
cLower = -inf
cUpper = -inf
```

Bei der Kompilierung mit sowohl **"/ O2"** und **/fp: strict** für die X86 Architektur, die Beispielprogramm gibt Folgendes aus:

```Output
cLower = -inf
cUpper = -3.40282e+38
```

### <a name="floating-point-special-values"></a>Spezielle Gleitkommazahlen-Punktwerte

Klicken Sie unter **/fp: präzise** und **/fp: strict**, Ausdrücke für die spezielle Werte (NaN, + unendlich, – unendlich,-0.0) Verhalten sich entsprechend der IEEE-754-Spezifikationen. Klicken Sie unter **fast**, das Verhalten dieser speziellen Werte ist möglicherweise inkonsistent mit IEEE-754.

Dieses Beispiel veranschaulicht das unterschiedliche Verhalten der speziellen Werte unter **/fp: präzise**, **/fp: strict** und **fast**:

```cpp
// fp_special_values.cpp
#include <stdio.h>
#include <cmath>

float gf0 = -0.0;

int main()
{
    float f1 = INFINITY;
    float f2 = NAN;
    float f3 = -INFINITY;
    bool a, b;
    float c, d, e;
    a = (f1 == f1);
    b = (f2 == f2);
    c = (f1 - f1);
    d = (f2 - f2);
    printf("INFINITY == INFINITY : %d\n", a);
    printf("NAN == NAN           : %d\n", b);
    printf("INFINITY - INFINITY  : %f\n", c);
    printf("NAN - NAN            : %f\n", d);

    e = gf0 / abs(f3);
    printf("std::signbit(-0.0/-INFINITY): %d\n", std::signbit(c));
    return 0;
}
```

Bei der Kompilierung mit **"/ O2"** **/fp: präzise** oder **"/ O2"** **/fp: strict** für X86 Architektur, die Ausgaben sind konsistent mit der IEEE-754 Spezifikation:

```Output
INFINITY == INFINITY : 1
NAN == NAN           : 0
INFINITY - INFINITY  : -nan(ind)
NAN - NAN            : -nan(ind)
std::signbit(-0.0/-INFINITY): 1
```

Bei der Kompilierung mit **"/ O2"** **fast** für X86 Architektur, die Ausgaben sind nicht konsistent mit IEEE-754:

```Output
INFINITY == INFINITY : 1
NAN == NAN           : 1
INFINITY - INFINITY  : 0.000000
NAN - NAN            : 0.000000
std::signbit(-0.0/-INFINITY): 0
```

### <a name="floating-point-algebraic-transformations"></a>Gleitkomma algebraische Transformationen

Klicken Sie unter **/fp: präzise** und **/fp: strict**, der Compiler führt keine mathematische Transformationen aus, es sei denn, die Transformation eine bitweise identischen Ergebnis garantiert ist. Der Compiler kann solche Transformationen unter Ausführen **fast**. Beispiel: der Ausdruck `a * b + a * c` in der Beispielfunktion `algebraic_transformation` kompiliert werden kann, in `a * (b + c)` unter **fast**. Diese Transformationen werden nicht ausgeführt, unter **/fp: präzise** oder **/fp: strict**, und der Compiler generiert `a * b + a * c`.

```cpp
float algebraic_transformation (float a, float b, float c)
{
    return a * b + a * c;
}
```

### <a name="floating-point-explicit-casting-points"></a>Gleitkomma explizite Umwandlung Punkte

Klicken Sie unter **/fp: präzise** und **/fp: strict**, der Compiler Rundet auf die Genauigkeit Code an vier bestimmten Punkten während der Auswertung von Ausdrücken: auf Zuweisungen an typenumwandlungen bei einem Gleitkommaargument übergeben wird, auf ein Funktionsaufruf ist, und wenn ein Gleitkommawert aus einem Funktionsaufruf zurückgegeben wird. Typenumwandlungen können verwendet werden, um explizit zwischen Berechnungen zu runden. Klicken Sie unter **fast**, generiert der Compiler keine explizite Umwandlungen an diesen Punkten Code Genauigkeit zu gewährleisten. Dieses Beispiel veranschaulicht das Verhalten unter verschiedenen **/fp** Optionen:

```cpp
float casting(float a, float b)
{
    return 5.0*((double)(a+b));
}
```

Beim Kompilieren mit **"/ O2"** **/fp: präzise** oder **"/ O2"** **/fp: strict**, sehen Sie, dass explizite Typumwandlungen, sowohl eingefügt werden die umwandeln und die Funktion zurückgeben Punkt im generierten Code für die X64 Architektur:

```asm
        addss    xmm0, xmm1
        cvtss2sd xmm0, xmm0
        mulsd    xmm0, QWORD PTR __real@4014000000000000
        cvtsd2ss xmm0, xmm0
        ret      0
```

Klicken Sie unter **"/ O2"** **fast** der generierte Code vereinfacht, da alle Typumwandlungen Optimierung entfernt werden:

```asm
        addss    xmm0, xmm1
        mulss    xmm0, DWORD PTR __real@40a00000
        ret      0
```

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Ausführliche Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **C/C++-** > **Codegenerierung** Eigenschaftenseite.

1. Ändern der **Gleitkommamodell** Eigenschaft.

### <a name="to-set-this-compiler-option-programmatically"></a>So legen Sie diese Compileroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.floatingPointModel%2A>.

## <a name="see-also"></a>Siehe auch

[Compileroptionen](compiler-options.md)<br/>
[Festlegen von Compileroptionen](setting-compiler-options.md)<br/>
[Microsoft Visual C++-Gleitkommaoptimierung](floating-point-optimization.md)<br/>
