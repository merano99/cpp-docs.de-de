---
title: Eigenschaft (C++ / CLI und C++ / CX)
ms.date: 10/12/2018
ms.topic: reference
f1_keywords:
- property_cpp
- property
helpviewer_keywords:
- property keyword [C++]
ms.assetid: cc79d2b2-f013-4d81-8252-eece97a18704
ms.openlocfilehash: df456ffb906eb6e0c68f3670692f292a8c20c407
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50526580"
---
# <a name="property--ccli-and-ccx"></a>Eigenschaft (C++ / CLI und C++ / CX)

Deklariert eine *Eigenschaft*, dies ist eine Memberfunktion, die verhält sich wie ein Datenmember oder Arrayelement erfolgt.

## <a name="all-runtimes"></a>Alle Laufzeiten

Sie können einen der folgenden Typen von Eigenschaften deklarieren.

*einfache Eigenschaft*<br/>
Erstellt standardmäßig eine *set-Accessor* , die den Wert der Eigenschaft weist einen *get-Accessor* , abruft, den Wert der Eigenschaft, und ein vom Compiler generierte private Datenmember, die den Wert der Eigenschaft enthält.

*Property-block*<br/>
Verwenden Sie diesen Typ zum Erstellen von benutzerdefinierten Get- und/oder Set-Zugriffsmethoden. Für die Eigenschaft gilt Lese-/Schreibzugriff, wenn get- und set-Accessoren definiert sind, sie ist schreibgeschützt, wenn nur der get-Accessor definiert ist, und lesegeschützt, wenn nur der set-Accessor definiert ist.

Sie müssen ein Datenmember explizit so deklarieren, dass es den Eigenschaftswert enthält.

*indizierte Eigenschaft*<br/>
Ein Property-Block, mit dem Sie einen Eigenschaftswert abrufen und festlegen können, der durch einen oder mehrere Indizes angegeben wird.

Sie können eine indizierte Eigenschaft, die entweder einen Namen für die benutzerdefinierte Eigenschaft erstellen oder ein *Standard* Eigenschaftenname. Der Name der Standardindexeigenschaft ist der Name der Klasse, in der die Eigenschaft definiert ist. Um eine Standardeigenschaft zu deklarieren, geben Sie die **Standard** Schlüsselwort anstelle eines Eigenschaftsnamens an.

Sie müssen ein Datenmember explizit so deklarieren, dass es den Eigenschaftswert enthält. Bei einer indizierten Eigenschaft ist das Datenmember in der Regel ein Array oder eine Sammlung.

### <a name="syntax"></a>Syntax

```cpp
property type property_name;

property type property_name {
   access-modifier type get() inheritance-modifier {property_body};
   access-modifier void set(type value) inheritance-modifier {property_body};
}

property type property_name[index_list] {
   access-modifier type get(index_list) inheritance-modifier {property_body};
   access-modifier void set(index_list, value) inheritance-modifier {property_body};
}

property type default[index_list] {
   access-modifier type get(index_list) inheritance-modifier {property_body};
   access-modifier void set(index_list, value) inheritance-modifier {property_body};
}
```

### <a name="parameters"></a>Parameter

*Typ*<br/>
Der Datentyp des Eigenschaftwerts und somit die Eigenschaft selbst.

*property_name*<br/>
Den Namen der Eigenschaft.

*Zugriffsmodifizierer*<br/>
Ein Zugangsqualifizierer. Gültige Qualifizierer sind **statische** und **virtuellen**.

Get oder Set-Zugriffsmethoden müssen nicht den gleichen der **virtuellen** Qualifizierer, aber sie müssen auf einigen der **statische** Qualifizierer.

*Vererbungsmodifizierer*<br/>
Ein Vererbungqualifizierer. Gültige Qualifizierer sind **abstrakte** und **versiegelten**.

*index_list*<br/>
Eine durch Kommata getrennte Liste von einem oder mehreren Indizes. Jeder Index besteht aus einem Indextyp und einem optionalen Bezeichner, der im Methodentext der Eigenschaft verwendet werden kann.

*Wert*<br/>
Der der Eigenschaft in einem set-Vorgang zuzuweisende Wert, oder der in einem get-Vorgang abzurufende Wert.

*property_body*<br/>
Der Methodentext der Eigenschaft der Set- oder Get-Zugriffsmethode. Die *Property_body* können die *Index_list* auf den zugrundeliegenden eigenschaftendatenmember zugreifen oder als Parameter in eine benutzerdefinierte Verarbeitung.

## <a name="windows-runtime"></a>Windows-Runtime

Weitere Informationen finden Sie unter [Eigenschaften (C++ / CX)](https://msdn.microsoft.com/library/windows/apps/hh755807.aspx).

### <a name="requirements"></a>Anforderungen

Compileroption: `/ZW`

## <a name="common-language-runtime"></a>Common Language Runtime

### <a name="syntax"></a>Syntax

```cpp
modifier property type property_name;

modifier property type property_name {
   modifier void set(type);
   modifier type get();
}
modifier property type property_name[index-list, value] {
   modifier void set(index-list, value);
   modifier type get(index-list);

modifier property type default[index];
}
```

### <a name="parameters"></a>Parameter

*Modifizierer*<br/>
Ein Modifizierer, der entweder für eine Eigenschaftendeklaration oder eine Get-/Set-Zugriffsmethode verwendet werden kann. Mögliche Werte sind **statische** und **virtuellen**.

*Typ*<br/>
Der Typ des Werts, der durch die Eigenschaft dargestellt wird.

*property_name*<br/>
Parameter für die Raise-Methode; muss der Signatur des Delegaten entsprechen.

*index_list*<br/>
Eine durch Kommata getrennte Liste von einem oder mehreren Indizes, die in eckigen Klammern (der Indexoperator, ([])) angegeben werden. Geben Sie für jeden Index einen Typ und optional einen Bezeichner an, der im Methodentext der Eigenschaft verwendet werden kann.

### <a name="remarks"></a>Hinweise

Das erste Syntaxbeispiel zeigt eine *einfache Eigenschaft*, die implizit deklariert wird, sowohl eine `set` und `get` Methode. Der Compiler erstellt automatisch ein privates Feld für die Speicherung des Werts der Eigenschaft.

Das zweite Syntaxbeispiel zeigt eine *Property-Block*, die explizit deklariert wird, sowohl eine `set` und `get` Methode.

Das dritte Syntaxbeispiel zeigt eine benutzerdefinierte *-Indexeigenschaft*. Eine Indexeigenschaft nimmt zusätzlich zu dem festzulegenden oder abzurufenden Wert Parameter. Sie müssen einen Namen für die Eigenschaft angeben. Im Gegensatz zu einer einfachen Eigenschaft müssen die `set`- und/oder `get`-Methoden einer Indexeigenschaft explizit definiert werden, und Sie müssen einen Namen für die Eigenschaft angeben.

Das vierte Syntax Beispiel zeigt eine *Standard* -Eigenschaft, die arrayähnlichen Zugriff auf eine Instanz des Typs bereitstellt. Das Schlüsselwort **Standard**, dient nur zum Angeben einer Standardeigenschaft. Der Name der Standardeigenschaft ist der Name des Typs, in dem die Eigenschaft definiert ist.

Die **Eigenschaft** Schlüsselwort kann in einer Klasse, Schnittstelle oder Werttyp angezeigt werden. Eine Eigenschaft kann über eine get-Funktion (schreibgeschützt), eine set-Funktion (lesegeschützt) oder beide (Lese-/Schreibzugriff) verfügen.

Ein Eigenschaftenname kann nicht mit dem Namen der verwalteten Klasse übereinstimmen, in der er enthalten ist. Der Rückgabetyp der Getter-Funktion muss dem Typ des letzten Parameters einer entsprechenden Setter-Funktion entsprechen.

Für Clientcode sieht eine Eigenschaft wie ein gewöhnliches Datenmember aus, und es kann anhand der gleichen Syntax wie bei einem Datenmember in sie geschrieben oder aus ihr gelesen werden.

Get und Set-Methoden müssen nicht den gleichen der **virtuellen** Modifizierer.

Der Zugriff auf die Get- und Set-Methode kann sich unterscheiden.

Die Definition einer Eigenschaftenmethode kann außerhalb des Klassentexts angezeigt werden, genau wie eine normale Methode.

Die Get- und Set-Methode für eine Eigenschaft müssen den gleichen der **statische** Modifizierer.

Eine Eigenschaft ist skalar, wenn ihre Get- und Set-Methoden der folgenden Beschreibung entsprechen:

- Die Get-Methode besitzt keine Parameter und hat den Rückgabetyp `T`.

- Die Set-Methode hat einen Parameter vom Typ `T`, und den Rückgabetyp **"void"**.

Es darf nur eine skalare Eigenschaft in einem Bereich mit dem gleichen Bezeichner deklariert werden. Skalare Eigenschaften können nicht überladen werden.

Wenn ein Eigenschaftendatenmember deklariert wird, fügt der Compiler ein Datenmember – auch als „Sicherungsspeicher“ bezeichnet – in der Klasse ein. Allerdings weist der Name des Datenmembers solch eine Form auf, dass Sie nicht auf das Element in der Datenquelle verweisen können, als handele es sich um ein tatsächliches Datenmember der enthaltenen Klasse. Zeigen Sie mithilfe von ildasm.exe die Metadaten für den Typ und den vom Compiler generierten Namen für den Sicherungsspeicher der Eigenschaft an.

Für die Accessormethoden sind unterschiedliche Zugriffsmöglichkeiten in einem Property-Block zulässig.  D. h., dass die Set-Methode öffentlich und die Get-Methode privat sein kann.  Es ist jedoch ein Fehler, wenn die Zugriffsmethode weniger restriktiven Zugriff hat als in der Deklaration der Eigenschaft selbst vermerkt ist.

**Eigenschaft** ist ein kontextbezogenes Schlüsselwort.  Weitere Informationen finden Sie unter [Kontextbezogene Schlüsselwörter](../windows/context-sensitive-keywords-cpp-component-extensions.md).

### <a name="requirements"></a>Anforderungen

Compileroption: `/clr`

### <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Deklaration und Verwendung eines Eigenschaftendatenmembers und eines Property-Blocks.  Es zeigt auch, dass eine Eigenschaftenzugriffsmethode außerhalb der Klasse definiert werden kann.

```cpp
// mcppv2_property.cpp
// compile with: /clr
using namespace System;
public ref class C {
   int MyInt;
public:

   // property data member
   property String ^ Simple_Property;

   // property block
   property int Property_Block {

      int get();

      void set(int value) {
         MyInt = value;
      }
   }
};

int C::Property_Block::get() {
   return MyInt;
}

int main() {
   C ^ MyC = gcnew C();
   MyC->Simple_Property = "test";
   Console::WriteLine(MyC->Simple_Property);

   MyC->Property_Block = 21;
   Console::WriteLine(MyC->Property_Block);
}
```

```Output
test

21
```

## <a name="see-also"></a>Siehe auch

[Komponentenerweiterungen für .NET und UWP](../windows/component-extensions-for-runtime-platforms.md)