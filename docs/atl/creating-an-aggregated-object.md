---
title: Erstellen eines aggregierten Objekts
ms.date: 11/04/2016
helpviewer_keywords:
- aggregation [C++], creating aggregated objects
- aggregate objects [C++], creating
ms.assetid: fc29d7aa-fd53-4276-9c2f-37379f71b179
ms.openlocfilehash: 5c655b8ced7738b30bf13d088cfadf11b5c65ef0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50449854"
---
# <a name="creating-an-aggregated-object"></a>Erstellen eines aggregierten Objekts

Aggregation Delegaten `IUnknown` Aufrufe, Angeben eines Zeigers auf des äußeren Objekts `IUnknown` auf das innere Objekt.

## <a name="to-create-an-aggregated-object"></a>Zum Erstellen eines aggregierten Objekts

1. Hinzufügen einer `IUnknown` Zeiger auf die Klasse Objekt, und initialisieren Sie es im Konstruktor auf NULL.

1. Außer Kraft setzen [FinalConstruct](../atl/reference/ccomobjectrootex-class.md#finalconstruct) So erstellen Sie das Aggregat.

1. Verwenden der `IUnknown` -Zeiger ist, definiert in Schritt 1, als der zweite Parameter für die [COM_INTERFACE_ENTRY_AGGREGATE](reference/com-interface-entry-macros.md#com_interface_entry_aggregate) Makros.

1. Außer Kraft setzen [FinalRelease](../atl/reference/ccomobjectrootex-class.md#finalrelease) Freigeben der `IUnknown` Zeiger.

> [!NOTE]
> Wenn Sie verwenden und veröffentlichen eine Schnittstelle von aggregierten Objekts während der `FinalConstruct`, sollten Sie hinzufügen, die [DECLARE_PROTECT_FINAL_CONSTRUCT](reference/aggregation-and-class-factory-macros.md#declare_protect_final_construct) Makro, um die Definition des Klassenobjekts.

## <a name="see-also"></a>Siehe auch

[Grundlagen von ARL COM-Objekten](../atl/fundamentals-of-atl-com-objects.md)

