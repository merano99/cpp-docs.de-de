---
title: Dialogfelder | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- modeless dialog boxes [MFC], MFC dialog boxes
- MFC, dialog boxes
- modal dialog boxes [MFC], MFC dialog boxes
- CDialog class [MFC], MFC dialog boxes
- MFC dialog boxes
ms.assetid: e4feea1a-8360-4ccb-9b84-507f1ccd9ef3
caps.latest.revision: "14"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 7e4417fc2d4714a249b04bb0c1d04e5642495835
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="dialog-boxes"></a>Dialogfelder
Anwendungen für Windows an, die häufig mit dem Benutzer in Dialogfeldern kommuniziert. Klasse [CDialog](../mfc/reference/cdialog-class.md) stellt eine Schnittstelle bereit, Verwalten von Dialogfeldern, die Visual C++-Dialog-Editor vereinfacht Dialogfelder entwerfen und erstellen ihre Dialogfeld-Vorlagenressourcen und Code-Assistenten vereinfachen den Prozess zu initialisieren und Überprüfen die Steuerelemente in einem Dialogfeld und die vom Benutzer eingegebenen Werte zu sammeln.  
  
 Dialogfelder enthalten Steuerelemente, einschließlich:  
  
-   Allgemeine Windows-Steuerelemente bearbeiten wie z. B. Textfelder, Druckknöpfe, Listenfelder, Kombinationsfelder, Struktursteuerelemente, List-Steuerelemente und Statusanzeigen.  
  
-   ActiveX-Steuerelemente.  
  
-   Ownerdrawn-Steuerelemente: Steuerelemente, die Sie für das Zeichnen Sie im Dialogfeld verantwortlich sind.  
  
 Die meisten Dialogfelder werden modal, die erfordern, dass des Benutzers das Dialogfeld zu schließen, bevor Sie mit einem beliebigen anderen Teil des Programms. Es ist jedoch möglich, nicht modale Dialogfelder zu erstellen, die können Benutzern das Arbeiten mit anderen Fenstern, während das Dialogfeld geöffnet ist. MFC unterstützt beide Arten von Dialogfeld mit der Klasse `CDialog`. Die Steuerelemente angeordnet werden und mithilfe einer Dialogfeldvorlagen-Ressource, die mit erstellt verwaltet die [Dialog-Editor](../windows/dialog-editor.md).  
  
 [Eigenschaftenblätter](../mfc/property-sheets-mfc.md), auch bekannt als Registerkarte Dialogfelder, Dialogfelder, die "Seiten" von unterschiedlichen Dialogfeld-Steuerelemente enthalten sind. Jede Seite hat einen Dateiordner "Register" oben. Auf einer Registerkarte setzt diese Seite auf den Anfang des Dialogfelds "".  
  
## <a name="what-do-you-want-to-know-more-about"></a>Was möchten Sie mehr erfahren  
  
-   [Beispiel: Anzeigen eines Dialogfelds mit einem Menübefehl](../mfc/example-displaying-a-dialog-box-via-a-menu-command.md)  
  
-   [Dialogfeld-Steuerelemente im framework](../mfc/dialog-box-components-in-the-framework.md)  
  
-   [Modale und nicht modale Dialogfelder](../mfc/modal-and-modeless-dialog-boxes.md)  
  
-   [Eigenschaftenblätter und Eigenschaftenseiten](../mfc/property-sheets-and-property-pages-mfc.md) in einem Dialogfeld  
  
-   [Erstellen der Dialogfeldressource](../mfc/creating-the-dialog-resource.md)  
  
-   [Erstellen einer Dialogfeldklasse mit Code-Assistenten](../mfc/creating-a-dialog-class-with-code-wizards.md)  
  
-   [Lebenszyklus eines Dialogfelds](../mfc/life-cycle-of-a-dialog-box.md)  
  
-   [Dialogdatenaustausch (DDX) und Überprüfung (DDV)](../mfc/dialog-data-exchange-and-validation.md)  
  
-   [Typsicherer Zugriff auf Steuerelemente in einem Dialogfeld](../mfc/type-safe-access-to-controls-in-a-dialog-box.md)  
  
-   [Zuordnen von Windows-Meldungen zu einer Klasse](../mfc/mapping-windows-messages-to-your-class.md)  
  
-   [Häufig überschreibbare Memberfunktionen](../mfc/commonly-overridden-member-functions.md)  
  
-   [Häufig hinzugefügte Memberfunktionen](../mfc/commonly-added-member-functions.md)  
  
-   [Allgemeine Dialogfeldklassen](../mfc/common-dialog-classes.md)  
  
-   [Dialogfelder in OLE](../mfc/dialog-boxes-in-ole.md)  
  
-   Erstellen Sie eine Anwendung, deren Benutzeroberfläche ein Dialogfeld wird: finden Sie unter der [CMNCTRL1](../visual-cpp-samples.md) oder [CMNCTRL2](../visual-cpp-samples.md) Beispielprogramme. Der Anwendungs-Assistent bietet diese Option auch.  
  
-   [Beispiele](../mfc/dialog-sample-list.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Benutzeroberflächenelemente](../mfc/user-interface-elements-mfc.md)