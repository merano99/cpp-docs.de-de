---
title: "Hinzufügen von Ereignishandlern für Dialogfeld-Steuerelemente | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- Dialog editor, adding event handlers to controls
- controls [C++], event handlers
- dialog box controls, events
- event handlers, for dialog box controls
ms.assetid: f9c70f24-ea6f-44df-82eb-78a2deaee769
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 4dd70693ebbdb7b286206f49fab3063c0aa72160
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="adding-event-handlers-for-dialog-box-controls"></a>Hinzufügen von Ereignishandlern für Dialogfeld-Steuerelemente
Für Project-Dialogfelder, die bereits einer Klasse zugeordnet sind, können Sie nutzen einige Tastenkombinationen bei der Erstellung von Ereignishandlern. Sie können schnell einen Handler für das Standardereignis des Steuerelements Benachrichtigung oder für eine relevante Windows-Meldung erstellen.  
  
#### <a name="to-create-a-handler-for-the-default-control-notification-event"></a>So erstellen einen Handler für das Standardereignis des Steuerelements Benachrichtigung  
  
1.  Doppelklicken Sie auf das Steuerelement. Der Text-Editor wird geöffnet.  
  
2.  Fügen Sie im Texteditor Steuerungscode Benachrichtigung-Handler hinzu.  
  
#### <a name="to-create-a-handler-for-any-applicable-windows-message"></a>So erstellen einen Handler für eine relevante Windows-Meldung  
  
1.  Klicken Sie auf das Steuerelement das Benachrichtigungsereignis behandelt werden soll.  
  
2.  In der [Fenster "Eigenschaften"](/visualstudio/ide/reference/properties-window), klicken Sie auf die **Steuerelementereignisse** Schaltfläche, um die Liste der allgemeinen Windows-Ereignisse, die mit dem Steuerelement verknüpfte anzuzeigen. Z. B. der Standard **OK** Schaltfläche auf der **zu** im Dialogfeld die folgenden Benachrichtigungsereignisse aufgelistet:  
  
 **BN_CLICKED**  
  
 **BN_DOUBLECLICKED**  
  
 **BN_KILLFOCUS**  
  
 **BN_SETFOCUS**  
  
    > [!NOTE]
    >  Klicken Sie Alternativ wählen Sie im Dialogfeld, und klicken Sie auf die **Steuerelementereignisse** Schaltfläche, um die Liste der allgemeinen Windows-Ereignisse für alle Steuerelemente im Dialogfeld anzuzeigen.  
  
3.  In der **Eigenschaften** Fenster, klicken Sie auf der rechten Spalte neben dem Ereignis zu behandeln, und wählen Sie dann den vorgeschlagenen Namen Benachrichtigungsereignis (z. B. **OnBnClickedOK** Handles **BN_CLICKED** ).  
  
    > [!NOTE]
    >  Alternativ können Sie einen Ereignishandlernamen Ihrer Wahl, anstatt die Auswahl des Standard-Ereignishandlernamens bereitstellen.  
  
     Nachdem Sie das Ereignis ausgewählt haben, wird von Visual Studio wird der Text-Editor geöffnet und zeigt den Ereignishandler Code. Im folgende Code wird z. B. für den standardmäßigen hinzugefügt **OnBnClickedOK**:  
  
 ```  
    void CAboutDlg::OnBnClickedOk(void)  
 { *// TODO: Add your control notification handler code here  
 }  
 ```  
  
 Gegebenenfalls Hinzufügen des ereignishandlers auf eine Klasse als eine Implementierung des Dialogfelds "", verwenden die [Ereignishandler-Assistent](../ide/event-handler-wizard.md). Weitere Informationen finden Sie unter [Hinzufügen eines Ereignishandlers](../ide/adding-an-event-handler-visual-cpp.md).  
  
 Informationen zum Hinzufügen von Ressourcen zu verwalteten Projekten finden Sie unter [Ressourcen in Desktop-Apps](https://msdn.microsoft.com/library/f45fce5x.aspx) in die *.NET Framework-Entwicklerhandbuch.* Informationen zum manuellen Hinzufügen von Ressourcendateien zu verwalteten Projekten, den Zugriff auf Ressourcen, zum Anzeigen statischer Ressourcen und Zuweisen von Ressourcenzeichenfolgen zu Eigenschaften, finden Sie unter [Erstellen von Ressourcendateien für Desktop-Apps](https://msdn.microsoft.com/library/xbx3z216.aspx). Informationen zur Globalisierung und Lokalisierung von Ressourcen in verwalteten apps finden Sie unter [Globalizing und Lokalisieren von .NET Framework-Anwendungen](https://msdn.microsoft.com/library/h6270d0z.aspx).  
  
### <a name="requirements"></a>Anforderungen  
 Win32  
  
## <a name="see-also"></a>Siehe auch  
 [Standardereignisse für Steuerelemente](../windows/default-control-events.md)   
 [Definieren von Membervariablen für Dialogfeld-Steuerelemente](../windows/defining-member-variables-for-dialog-controls.md)   
 [Dialogfeld-Steuerelemente und Variablentypen](../ide/dialog-box-controls-and-variable-types.md)   
 [Hinzufügen einer Klasse](../ide/adding-a-class-visual-cpp.md)   
 [Hinzufügen einer Memberfunktion](../ide/adding-a-member-function-visual-cpp.md)   
 [Hinzufügen einer Membervariablen](../ide/adding-a-member-variable-visual-cpp.md)   
 [Überschreiben einer virtuellen Funktion](../ide/overriding-a-virtual-function-visual-cpp.md)   
 [MFC-Meldungshandler](../mfc/reference/adding-an-mfc-message-handler.md)
