---
title: /Zc:wchar_t (wchar_t ist der systemeigene Typ)
ms.date: 03/01/2018
f1_keywords:
- VC.Project.VCCLWCECompilerTool.TreatWChar_tAsBuiltInType
- VC.Project.VCCLCompilerTool.TreatWChar_tAsBuiltInType
- /Zc:wchar_t
helpviewer_keywords:
- /Zc compiler options [C++]
- -Zc compiler options [C++]
- wchar_t type
- Conformance compiler options
- Zc compiler options [C++]
ms.assetid: b0de5a84-da72-4e5a-9a4e-541099f939e0
ms.openlocfilehash: 13d25a73a0c70789e8b860607e9f222e69ae6d36
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50537929"
---
# <a name="zcwchart-wchart-is-native-type"></a>/Zc:wchar_t (wchar_t ist der systemeigene Typ)

Analysieren Sie `wchar_t` als integrierten Typ entsprechend dem C++-Standard.

## <a name="syntax"></a>Syntax

> **/Zc:wchar_t**[**-**]

## <a name="remarks"></a>Hinweise

Wenn **/Zc: wchar_t** aktiviert ist, `wchar_t` ist ein Schlüsselwort für einen integrierten ganzzahligen Typ im als C++ kompilierten Code. Wenn **/Zc:** (mit einem Minuszeichen) wird angegeben, oder im Code als C kompiliert, `wchar_t` ist kein integrierter Typ. Stattdessen `wchar_t` ist definiert als eine `typedef` für `unsigned short` in die kanonische Header STDDEF.h definiert ist. (Die Microsoft-Implementierung definiert es in einem anderen Header, der vom stddef.h berücksichtigt wird und andere standard-Header.)

Wir empfehlen nicht **/Zc:** , da der C++-Standard, erfordert `wchar_t` ein integrierter Typ sein. Die Verwendung der `typedef`-Version kann Portabilitätsprobleme verursachen. Wenn Sie ein von früheren Versionen von Visual C++ Upgrade und Compilerfehler auftreten, [C2664](../../error-messages/compiler-errors-2/compiler-error-c2664.md) , da der Code versucht, eine implizite Konvertierung einer `wchar_t` zu `unsigned short`, es wird empfohlen, die Sie ändern den Code, um stattdessen den Fehler zu beheben Einstellung **/Zc:**.

Die **/Zc: wchar_t** Option ist standardmäßig in C++-Kompilierungen und wird in C++-Kompilierungen ignoriert. Die [/ PERMISSIVE--](permissive-standards-conformance.md) Option hat keine Auswirkungen auf **/Zc: wchar_t**.

Microsoft implementiert `wchar_t` als 2-Byte-Wert ohne Vorzeichen. In den Microsoft-spezifischen systemeigenen Typ zugeordnet `__wchar_t`. Weitere Informationen zu `wchar_t`, finden Sie unter [Datentypbereiche](../../cpp/data-type-ranges.md) und [Basistypen](../../cpp/fundamental-types-cpp.md).

Wenn Sie neuen Code schreiben, der mit älterem Code zusammenwirken, die noch verwendet die `typedef` Version des `wchar_t`, können Sie Überladungen für beide Bereitstellen der `unsigned short` und `__wchar_t` Variationen des `wchar_t`, sodass Ihr Code mit verknüpft werden kann Code mit kompiliert **/Zc: wchar_t** oder ohne kompilierten Code. Andernfalls müssen Sie bieten zwei verschiedene builds der Bibliothek, eine mit und ohne **/Zc: wchar_t** aktiviert. Allerdings wird in beiden Fällen empfohlen, den älteren und den neuen Code mit demselben Compiler zu erstellen. Kombinieren Sie niemals die Binärdateien, die mit unterschiedlichen Compilern erstellt wurden.

Wenn **/Zc: wchar_t** angegeben wird,  **\_WCHAR\_T\_definierte** und  **\_NATIVE\_WCHAR\_T\_definierte** Symbole definiert sind. Weitere Informationen finden Sie unter [Predefined Macros](../../preprocessor/predefined-macros.md).

Wenn Ihr Code die globale Compiler-COM-Funktionen, verwendet da **/Zc: wchar_t** ist jetzt auf standardmäßig, es wird empfohlen, dass Sie explizite Verweise auf comsupp.lib ändern (entweder über die [kommentieren Pragma](../../preprocessor/comment-c-cpp.md) oder auf der über die Befehlszeile) auf comsuppw.lib oder comsuppwd.lib. (Wenn Sie mit der Kompilierung müssen **/Zc:**, sollten Sie comsupp.lib verwenden.) Wenn Sie die comdef.h-Headerdatei einfügen, wird die richtige Bibliothek für Sie angegeben. Weitere Informationen zur Compiler-COM-Unterstützung finden Sie unter [Compiler COM unterstützt](../../cpp/compiler-com-support.md).

Die `wchar_t` integrierter Typ wird nicht unterstützt, wenn Sie C-Code kompilieren. Weitere Informationen über Konformitätsprobleme mit Visual C++ finden Sie unter [Nonstandard Behavior](../../cpp/nonstandard-behavior.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Ausführliche Informationen finden Sie unter [Working with Project Properties (Arbeiten mit Projekteigenschaften)](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **C/C++-** > **Sprache** Seite.

1. Ändern der **Wchar_t als integrierten Typ behandeln** Eigenschaft.

### <a name="to-set-this-compiler-option-programmatically"></a>So legen Sie diese Compileroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.TreatWChar_tAsBuiltInType%2A>.

## <a name="see-also"></a>Siehe auch

[/Zc (Übereinstimmung)](../../build/reference/zc-conformance.md)<br/>
