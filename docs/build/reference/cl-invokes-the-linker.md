---
title: 'CL: Starten des Linkers'
ms.date: 11/04/2016
f1_keywords:
- cl
helpviewer_keywords:
- compiling source code [C++], without linking
- invoking linker from the compiler
- LINK tool [C++], invoking from CL compiler
- cl.exe compiler [C++], compiling without linking
- cl.exe compiler [C++], controlling linker
ms.assetid: eae47ef7-09eb-40c9-b318-7c714cd452fc
ms.openlocfilehash: e071209bd09fea17082379bf3f2486866b52c548
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50447202"
---
# <a name="cl-invokes-the-linker"></a>CL: Starten des Linkers

CL Ruft den Linker automatisch nach dem Kompilieren, es sei denn, die/c-Option verwendet wird. CL wird an den Linker übergeben, die Namen der OBJ-Dateien, die während der Kompilierung erstellt und die Namen der anderen Dateien, die in der Befehlszeile angegeben. Der Linker verwendet die in der Umgebungsvariablen LINK aufgeführten Optionen. Sie können die Option/Link verwenden, die Linkeroptionen in der CL-Befehlszeile angeben. Optionen, die die Option/Link folgen, überschreiben die in der LINK-Umgebungsvariablen. Die Optionen in der folgenden Tabelle unterdrücken, verknüpfen.

|Option|Beschreibung|
|------------|-----------------|
|/c|Kompilieren ohne Verknüpfen|
|/ E/EP, / P|Vorverarbeiten Sie, ohne kompilieren und verknüpfen|
|/Zg|Funktionsprototypen generieren|
|/Zs|Überprüfen Sie syntax|

Weitere Informationen zum Verknüpfen, finden Sie unter [Optionen des Linkers](../../build/reference/linker-options.md).

## <a name="example"></a>Beispiel

Angenommen, Sie drei C-Quelldateien kompilieren: MAIN.c MOD1.c und MOD2.c. Jede Datei enthält einen Aufruf einer Funktion, die in einer anderen Datei definiert:

- Ruft die Funktion auf MAIN.c `func1` in MOD1.c und der Funktion `func2` in MOD2.c auf.

- MOD1.c Aufrufe der Standardbibliotheksfunktionen `printf_s` und `scanf_s`.

- Ruft die MOD2.c Grafikfunktionen `myline` und `mycircle`, die in der Bibliothek MYGRAPH.lib definiert werden.

Um dieses Programm zu erstellen, kompilieren Sie mit der folgenden Befehlszeile ein:

```
CL MAIN.c MOD1.C MOD2.C MYGRAPH.lib
```

CL zuerst die C-Quelldateien kompiliert und erstellt die Objektdateien MAIN.obj MOD1.obj und MOD2.obj. Der Compiler fügt den Namen der Standardbibliothek in jeder OBJ-Datei. Weitere Informationen finden Sie unter [Use Run-Time Library](../../build/reference/md-mt-ld-use-run-time-library.md).

CL übergibt die Namen OBJ-Dateien, zusammen mit dem Namen MYGRAPH.lib, an dem Linker an. Der Linker löst die externe Verweise wie folgt aus:

1. In den Verweis auf MAIN.obj `func1` wird aufgelöst, mit der Definition aus MOD1.obj; der Verweis auf `func2` wird mit der Definition in MOD2.obj aufgelöst.

1. In den Verweisen auf MOD1.obj `printf_s` und `scanf_s` mit den Definitionen in der Bibliothek, die der Linker sucht mit dem Namen MOD1.obj aufgelöst werden.

1. In den Verweisen auf MOD2.obj `myline` und `mycircle` mit den Definitionen in MYGRAPH.lib aufgelöst werden.

## <a name="see-also"></a>Siehe auch

[Compileroptionen](../../build/reference/compiler-options.md)<br/>
[Festlegen von Compileroptionen](../../build/reference/setting-compiler-options.md)