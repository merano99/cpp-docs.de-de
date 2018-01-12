---
title: Muss ich von CObject neue Klassen ableiten? | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CObject
dev_langs: C++
helpviewer_keywords:
- derived classes [MFC], from CObject
- CObject class [MFC], when to use
ms.assetid: 26021031-feaf-424c-80d1-9547c4409d6a
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: c485bba4d62d279b0f17b887080284940a8bbdd5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="do-i-have-to-derive-new-classes-from-cobject"></a>Muss ich von CObject neue Klassen ableiten?
Nein, stimmen Sie nicht.  
  
 Leiten Sie eine Klasse von [CObject](../mfc/reference/cobject-class.md) Wenn Sie die Funktionen sie bereitstellt benötigen, z. B. Serialisierung oder dynamische Creatability. Viele Datenklassen müssen in Dateien, serialisiert werden, weshalb es oft eine gute Idee, daraus ableiten kann `CObject`. Ein Beispiel für eine Klasse vom abgeleitet `CObject`, finden Sie unter der [Scribble-Beispiel](../visual-cpp-samples.md).  
  
## <a name="see-also"></a>Siehe auch  
 [CObject-Klasse: Häufig gestellte Fragen](../mfc/cobject-class-frequently-asked-questions.md)