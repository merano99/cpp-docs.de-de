---
title: Funktionsaufruf (C)
ms.date: 11/04/2016
helpviewer_keywords:
- function calls, C functions
- functions [C], calling
- function calls
ms.assetid: 35c66719-3f15-4d3b-97da-4e19dc97b308
ms.openlocfilehash: 46e010ed625e23aa6c21b8c78280b714c68582b8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50478116"
---
# <a name="function-call-c"></a>Funktionsaufruf (C)

Ein *Funktionsaufruf* ist ein Ausdruck, der den Namen der aufgerufenen Funktion oder den Wert eines Funktionszeigers und optional die Argumente, die der Funktion übergeben werden, enthält.

## <a name="syntax"></a>Syntax

*postfix-expression*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*postfix-expression*  **(**  *argument-expression-list*<sub>opt</sub> **)**

*argument-expression-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*assignment-expression*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*argument-expression-list* **,** *assignment-expression*

Der *postfix-expression* muss eine Funktionsadresse ergeben (z.B. einen Funktionsbezeichner oder Funktionszeigerwert), und die *argument-expression-list* ist eine Ausdrucksliste (durch Kommas getrennt), deren Werte (die „Argumente“) an die Funktion übergeben werden. Das *argument-expression-list*-Argument kann leer sein.

Ein Funktionsaufrufausdruck hat den Wert und Typ des Rückgabewerts der Funktion. Eine Funktion kann kein Objekt des Arraytyps zurückgeben. Wenn der Rückgabetyp der Funktion `void` ist (die Funktion also so deklariert wurde, dass sie niemals einen Wert zurückgibt), hat der Funktionsaufrufausdruck ebenfalls den Typ `void`. (Weitere Informationen finden Sie unter [Funktionsaufrufe](../c-language/function-calls.md).)

## <a name="see-also"></a>Siehe auch

[Funktionsaufrufoperator: ()](../cpp/function-call-operator-parens.md)