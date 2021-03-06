---
title: 'Gewusst wie: Auffangen von Windows Forms-Ereignissen aus systemeigenen C++-Klassen'
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- event handling, managed/native interop
- event handling, sinking .NET in C++
- event handling, .NET/native interop
- event handling, Windows Forms in C++
ms.assetid: 6e30ddee-d058-4c8d-9956-2a43d86f19d5
ms.openlocfilehash: 1bc601a4dbd7a51695b6964ab4d0ee47531c1b2b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50555908"
---
# <a name="how-to-sink-windows-forms-events-from-native-c-classes"></a>Gewusst wie: Auffangen von Windows Forms-Ereignissen aus systemeigenen C++-Klassen

Sie können native C++-Klassen zum Empfangen von Rückrufen von verwalteten Ereignissen in Windows Forms-Steuerelemente oder andere Formen mit das Format der MFC-Makros aktivieren. Auffangen von Ereignissen in Ansichten und Dialogfelder ist ähnlich wie die gleiche Aufgabe für Steuerelemente.

Zu diesem Zweck müssen Sie:

- Fügen Sie eine `OnClick` -Ereignishandler, um das Steuerelement mit [MAKE_DELEGATE](../mfc/reference/delegate-and-interface-maps.md#make_delegate).

- Erstellen Sie ein Delegat-Zuordnung mit [BEGIN_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#begin_delegate_map), [END_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#end_delegate_map), und [EVENT_DELEGATE_ENTRY](../mfc/reference/delegate-and-interface-maps.md#event_delegate_entry).

In diesem Beispiel wird die Arbeit aus weiterhin [wie: tun DDX-/DDV-Datenbindung mit Windows Forms](../dotnet/how-to-do-ddx-ddv-data-binding-with-windows-forms.md).

Nun, verknüpfen Sie Ihr MFC-Steuerelement (`m_MyControl`) mit einem verwalteten Ereignishandlerdelegaten aufgerufen `OnClick` für den verwalteten <xref:System.Windows.Forms.Control.Click> Ereignis.

### <a name="to-attach-the-onclick-event-handler"></a>So fügen Sie dem OnClick-Ereignishandler an:

1. Fügen Sie den folgenden Code, um die Implementierung von "bool" CMFC01Dlg:: OnInitDialog:

    ```
    m_MyControl.GetControl()->button1->Click += MAKE_DELEGATE( System::EventHandler, OnClick );
    ```

1. Fügen Sie den folgenden Code, mit dem öffentlichen Abschnitt in der Deklaration der Klasse CMFC01Dlg: öffentliche CDialog.

    ```
    // delegate map
    BEGIN_DELEGATE_MAP( CMFC01Dlg )
    EVENT_DELEGATE_ENTRY( OnClick, System::Object^, System::EventArgs^ )
    END_DELEGATE_MAP()

    void OnClick( System::Object^ sender, System::EventArgs^ e );
    ```

1. Fügen Sie abschließend die Implementierung für `OnClick` auf die Datei "CMFC01Dlg.cpp":

    ```
    void CMFC01Dlg::OnClick(System::Object^ sender, System::EventArgs^ e)
    {
        AfxMessageBox(_T("Button clicked"));
    }
    ```

## <a name="see-also"></a>Siehe auch

[MAKE_DELEGATE](../mfc/reference/delegate-and-interface-maps.md#make_delegate)<br/>
[BEGIN_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#begin_delegate_map)<br/>
[END_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#end_delegate_map)<br/>
[EVENT_DELEGATE_ENTRY](../mfc/reference/delegate-and-interface-maps.md#event_delegate_entry)