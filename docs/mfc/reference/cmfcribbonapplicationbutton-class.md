---
title: CMFCRibbonApplicationButton Klasse | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCRibbonApplicationButton
- AFXRIBBONBAR/CMFCRibbonApplicationButton
- AFXRIBBONBAR/CMFCRibbonApplicationButton::CMFCRibbonApplicationButton
- AFXRIBBONBAR/CMFCRibbonApplicationButton::SetImage
dev_langs: C++
helpviewer_keywords:
- CMFCRibbonApplicationButton [MFC], CMFCRibbonApplicationButton
- CMFCRibbonApplicationButton [MFC], SetImage
ms.assetid: beb81757-fabd-4641-9130-876ba8505b78
caps.latest.revision: "25"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 11f8b9f9c6a260f47e1e43a35c78073312b48041
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="cmfcribbonapplicationbutton-class"></a>CMFCRibbonApplicationButton-Klasse
Implementiert eine spezielle Schaltfläche in der oberen linken Ecke des Anwendungsfensters. Wenn sie angeklickt wird, öffnet die Schaltfläche ein Menü, das normalerweise allgemeine **Datei** -Befehle wie **Öffnen**, **Speichern**und **Beenden**enthält.  
  
## <a name="syntax"></a>Syntax  
  
```  
class CMFCRibbonApplicationButton : public CMFCRibbonButton  
```  
  
## <a name="members"></a>Mitglieder  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CMFCRibbonApplicationButton::CMFCRibbonApplicationButton](#cmfcribbonapplicationbutton)|Erstellt und initialisiert ein `CMFCRibbonApplicationButton`-Objekt.|  
  
### <a name="public-methods"></a>Öffentliche Methoden  
  
|Name|Beschreibung|  
|----------|-----------------|  
|`CMFCRibbonApplicationButton::CreateObject`|Wird vom Framework verwendet, um eine dynamische Instanz dieses Klassentyps zu erstellen.|  
|`CMFCRibbonApplicationButton::GetThisClass`|Durch das Framework verwendet wird, um einen Zeiger auf die [CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md) -Objekt, das diesem Klassentyp zugeordnet ist.|  
|[CMFCRibbonApplicationButton::SetImage](#setimage)|Weist ein Bild der Schaltfläche des Menübands-Anwendung.|  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie verschiedene Methoden in der `CMFCRibbonApplicationButton` Klasse. Im Beispiel wird gezeigt, wie die Anwendungsschaltfläche ein Bild zuzuweisen und zum Festlegen der QuickInfo. Dieser Codeausschnitt ist Teil des [Draw Client-Beispiels](../../visual-cpp-samples.md).  
  
 [!code-cpp[NVC_MFC_DrawClient#4](../../mfc/reference/codesnippet/cpp/cmfcribbonapplicationbutton-class_1.h)]  
[!code-cpp[NVC_MFC_DrawClient#5](../../mfc/reference/codesnippet/cpp/cmfcribbonapplicationbutton-class_2.cpp)]  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)  
  
 [CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)  
  
 [CMFCRibbonApplicationButton](../../mfc/reference/cmfcribbonapplicationbutton-class.md)  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** afxRibbonBar.h  
  
##  <a name="cmfcribbonapplicationbutton"></a>CMFCRibbonApplicationButton::CMFCRibbonApplicationButton  
 Erstellt und initialisiert ein [CMFCRibbonApplicationButton](../../mfc/reference/cmfcribbonapplicationbutton-class.md) Objekt.  
  
```  
CMFCRibbonApplicationButton();  
CMFCRibbonApplicationButton(UINT uiBmpResID);  
  CMFCRibbonApplicationButton(HBITMAP hBmp);
```  
  
### <a name="parameters"></a>Parameter  
 `uiBmpResID`  
 Die Ressourcen-ID des Bilds auf der Schaltfläche angezeigt werden sollen.  
  
 `hBmp`  
 Ein Handle für eine Bitmap, die auf die Anwendungsschaltfläche angezeigt.  
  
### <a name="remarks"></a>Hinweise  
 Die Anwendung Menübandschaltfläche ist eine spezielle Schaltfläche, die in der oberen linken Ecke des Anwendungsfensters befindet. Wenn ein Benutzer auf diese Schaltfläche klickt, wird die Anwendung öffnet ein Menü, das normalerweise allgemeine **Datei** Befehle, wie z. B. **öffnen**, **speichern**, und **beenden**.  
  
##  <a name="setimage"></a>CMFCRibbonApplicationButton::SetImage  
 Weist ein Bild der Schaltfläche für die Anwendung an.  
  
```  
void SetImage(UINT uiBmpResID);  
void SetImage(HBITMAP hBmp);
```  
  
### <a name="parameters"></a>Parameter  
 [in] `uiBmpResID`  
 Die Ressourcen-ID des Bilds auf der Schaltfläche angezeigt werden sollen.  
  
 [in] `hBmp`  
 Ein Handle für eine Bitmap, die auf die Anwendungsschaltfläche angezeigt.  
  
### <a name="remarks"></a>Hinweise  
 Verwenden Sie diese Methode, um die Menübandschaltfläche Anwendung ein neues Image zuweisen, nachdem Sie die Schaltfläche "" erstellt. Die Anwendungsschaltfläche befindet sich in der oberen linken Ecke des Anwendungsfensters.  
  
## <a name="see-also"></a>Siehe auch  
 [Hierarchiediagramm](../../mfc/hierarchy-chart.md)   
 [Klassen](../../mfc/reference/mfc-classes.md)   
 [CMFCRibbonButton-Klasse](../../mfc/reference/cmfcribbonbutton-class.md)