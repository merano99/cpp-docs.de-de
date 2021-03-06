---
title: Compilerwarnung (Stufe 1) C4067
ms.date: 11/04/2016
f1_keywords:
- C4067
helpviewer_keywords:
- C4067
ms.assetid: 1d10353e-8cd5-4b01-9184-a06189b965a4
ms.openlocfilehash: 012866e328433ec9511782c26a39265481ff4940
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50541186"
---
# <a name="compiler-warning-level-1-c4067"></a>Compilerwarnung (Stufe 1) C4067

> Unerwartetes Token nach Präprozessordirektive - Zeilenvorschub erwartet.

## <a name="remarks"></a>Hinweise

Der Compiler gefunden und zusätzliche Zeichen, die nach einer Präprozessordirektive ignoriert. Dies kann durch beliebige unerwartete Zeichen verursacht werden, obwohl eine häufige Ursache ein vereinzelten Semikolon nach der Direktive ist. Kommentare sind nicht dazu führen, dass diese Warnung. Die **/Za** -Compileroption kann diese Warnung für weitere präprozessoranweisungen, als die Standardeinstellung.

## <a name="example"></a>Beispiel

```cpp
// C4067a.cpp
// compile with: cl /EHsc /DX /W1 /Za C4067a.cpp
#include <iostream>
#include <string> s     // C4067
#if defined(X);         // C4067
std::string s{"X is defined"};
#else
std::string s{"X is not defined"};
#endif;                 // C4067 only under /Za
int main()
{
    std::cout << s << std::endl;
}
```

Um diese Warnung zu beheben, löschen Sie die vereinzelten Zeichen, oder verschieben in einen Kommentarblock. Bestimmte Warnungen C4067 können deaktiviert werden, durch das Entfernen der **/Za** -Compileroption.

```cpp
// C4067b.cpp
// compile with: cl /EHsc /DX /W1 C4067b.cpp
#include <iostream>
#include <string>
#if defined(X)
std::string s{"X is defined"};
#else
std::string s{"X is not defined"};
#endif
int main()
{
    std::cout << s << std::endl;
}
```