---
title: "Festlegen von Funktionalitätsebenen | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- CObject class [MFC], adding functionality to derived classes
- runtime [MFC], class information
- serialization [MFC], Cobject
- dynamic creation support
- levels [MFC], functionality in CObject
- run-time class [MFC], information support
- levels [MFC]
ms.assetid: 562669ba-c858-4f66-b5f1-b3beeea4f486
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 13a2897d5e442794198870e7f6bed36196744888
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="specifying-levels-of-functionality"></a>Festlegen von Funktionalitätsebenen
In diesem Artikel wird beschrieben, wie die folgenden Grade an Funktionalität zum Hinzufügen Ihrer [CObject](../mfc/reference/cobject-class.md)-Klasse abgeleitet:  
  
-   [Laufzeit Klasseninformationen](#_core_to_add_run.2d.time_class_information)  
  
-   [Unterstützung für dynamische Erstellung](#_core_to_add_dynamic_creation_support)  
  
-   [Unterstützung von Serialisierung](#_core_to_add_serialization_support)  
  
 Eine allgemeine Beschreibung des `CObject` Funktionen finden Sie im Artikel [Ableiten einer Klasse von CObject](../mfc/deriving-a-class-from-cobject.md).  
  
-   [Laufzeit Klasseninformationen](#_core_to_add_run.2d.time_class_information)  
#### <a name="_core_to_add_run.2d.time_class_information"></a>Laufzeit Klasseninformationen hinzufügen  
  
1.  Leiten Sie eine Klasse von `CObject`gemäß der Beschreibung in der [Ableiten einer Klasse von CObject](../mfc/deriving-a-class-from-cobject.md) Artikel.  
  
2.  Verwenden der `DECLARE_DYNAMIC` Makros in der Klassendeklaration, wie hier gezeigt:  
  
     [!code-cpp[NVC_MFCCObjectSample#2](../mfc/codesnippet/cpp/specifying-levels-of-functionality_1.h)]  
  
3.  Verwenden der `IMPLEMENT_DYNAMIC` Makro in der Implementierungsdatei (. CPP) der Klasse. Dieses Makro akzeptiert als Argumente den Namen der Klasse und ihre Basisklasse wie folgt:  
  
     [!code-cpp[NVC_MFCCObjectSample#3](../mfc/codesnippet/cpp/specifying-levels-of-functionality_2.cpp)]  
  
> [!NOTE]
>  Immer put `IMPLEMENT_DYNAMIC` in der Implementierungsdatei (. CPP) für die Klasse. Die `IMPLEMENT_DYNAMIC` Makro nur einmal während der Kompilierung ausgewertet werden und sollte daher nicht in einer Schnittstellendatei verwendet werden (. H), konnte möglicherweise in mehr als eine Datei enthalten sein.  
  
#### <a name="_core_to_add_dynamic_creation_support"></a>So fügen Sie Unterstützung für dynamische Erstellung hinzu  
  
1.  Leiten Sie eine Klasse von `CObject`.  
  
2.  Verwenden der `DECLARE_DYNCREATE` Makros in der Klassendeklaration.  
  
3.  Definieren Sie einen Konstruktor ohne Argumente (Standardkonstruktor).  
  
4.  Verwenden der `IMPLEMENT_DYNCREATE` Makro in der Implementierungsdatei der Klasse.  
  
#### <a name="_core_to_add_serialization_support"></a>Zum Hinzufügen der Serialisierungsunterstützung  
  
1.  Leiten Sie eine Klasse von `CObject`.  
  
2.  Überschreiben Sie die `Serialize` Memberfunktion.  
  
    > [!NOTE]
    >  Beim Aufrufen `Serialize` direkt, d. h., Sie sollten keine serialisiert das Objekt über einen polymorphen Zeiger, überspringen Sie die Schritte 3 bis 5.  
  
3.  Verwenden der `DECLARE_SERIAL` Makros in der Klassendeklaration.  
  
4.  Definieren Sie einen Konstruktor ohne Argumente (Standardkonstruktor).  
  
5.  Verwenden der `IMPLEMENT_SERIAL` Makro in der Implementierungsdatei der Klasse.  
  
> [!NOTE]
>  Ein "polymorpher Zeiger" verweist auf ein Objekt einer Klasse (rufen sie ein) oder auf ein Objekt einer beliebigen Klasse abgeleitet wurde. ein (z. B. B). Um einen polymorphen Zeiger zu serialisieren, muss das Framework die Laufzeitklasse des Objekts bestimmen, es (B) serialisiert, da es ein Objekt einer Klasse, die von einer Basisklasse (A) abgeleitet werden kann.  
  
 Weitere Informationen zum Aktivieren der Serialisierung, wenn Sie eine Klasse von ableiten `CObject`, finden Sie in den Artikeln [Dateien in MFC](../mfc/files-in-mfc.md) und [Serialisierung](../mfc/serialization-in-mfc.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Ableiten einer Klasse von CObject](../mfc/deriving-a-class-from-cobject.md)