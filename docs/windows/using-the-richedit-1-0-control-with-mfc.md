---
title: Verwenden des RichEdit 1.0-Steuerelements mit MFC | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- RichEdit 1.0 control
- rich edit controls, RichEdit 1.0
ms.assetid: 5a9060dd-44d8-4ef3-956e-16152f7e23d2
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: f8085eb8b28ece4f0ca24d00c33b8809aa412da5
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="using-the-richedit-10-control-with-mfc"></a>Verwenden des RichEdit 1.0-Steuerelements mit MFC
Um eine RichEdit-Steuerelement verwenden, müssen Sie zuerst Aufrufen [AfxInitRichEdit2](../mfc/reference/application-information-and-management.md#afxinitrichedit2) beim Laden der RichEdit 2.0-Steuerelement (RICHED20. (DLL), oder rufen Sie [AfxInitRichEdit](../mfc/reference/application-information-and-management.md#afxinitrichedit) beim Laden des älteren RichEdit 1.0-Steuerelements (RICHED32. (DLL).  
  
 Möglicherweise verwenden Sie die aktuelle [CRichEditCtrl](../mfc/reference/cricheditctrl-class.md) Klasse mit dem älteren RichEdit 1.0-Steuerelement, aber **CRichEditCtrl** dient nur zur Unterstützung des RichEdit 2.0-Steuerelements. Da RichEdit 1.0 und 2.0 RichEdit sehr ähnlich sind, funktionieren die meisten Methoden; Beachten Sie jedoch, dass es gibt einige Unterschiede zwischen den Steuerelementen 1.0 und 2.0, sodass einige Methoden möglicherweise voll oder fehlerhaft funktionsfähig oder gar nicht funktionsfähig.  
  
## <a name="requirements"></a>Anforderungen  
 MFC  
  
## <a name="see-also"></a>Siehe auch  
 [Problembehandlung für den Dialog-Editor](../windows/troubleshooting-the-dialog-editor.md)   
 [Dialog-Editor](../windows/dialog-editor.md)
