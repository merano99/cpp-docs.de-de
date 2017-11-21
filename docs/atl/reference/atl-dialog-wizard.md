---
title: ATL-Dialogfeld-Assistent | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: vc.codewiz.class.atl.dlg.overview
dev_langs: C++
helpviewer_keywords:
- ATL projects, adding dialog resources
- ATL Dialog Wizard
ms.assetid: b0b9ace5-83c9-40d3-82c3-eb6293f10583
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 003cda9f3b0916cb7c86dfce874840268a64dbff
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="atl-dialog-wizard"></a>ATL-Dialogfeld-Assistent
Dieser Assistent fügt dem Projekt abgeleitet ATL-Dialogfeldobjekt [CAxDialogImpl](../../atl/reference/caxdialogimpl-class.md). Ein Dialogfeld abgeleitet `CAxDialogImpl` ActiveX-Steuerelemente hosten können.  
  
 Der Assistent erstellt eine Dialogfeldressource Standardwert **OK** und **"Abbrechen"** Schaltflächen. Können die Dialogressource bearbeiten und Hinzufügen von ActiveX-Steuerelemente mithilfe der [Dialog-Editor](../../windows/dialog-editor.md) in der Ressourcenansicht.  
  
 Fügt der Assistent in der Headerdatei eine [meldungszuordnung](../../atl/message-maps-atl.md) und Deklarationen für die Behandlung des Standardwerts click-Ereignisse. Finden Sie unter [Implementieren eines Dialogfelds](../../atl/implementing-a-dialog-box.md) für Weitere Informationen über ATL-Dialogfelder.  
  
 **Kurzname**  
 Legt den abgekürzten Namen für das ATL-Dialogfeld-Objekt. Der Name, den Sie angeben, bestimmt den Klassennamen und den Dateinamen (cpp- und h), wenn Sie diese Felder einzeln ändern.  
  
 `Class`  
 Legt den Namen der Klasse erstellt werden soll. Dieser Name basiert auf den Namen, die Sie, in angeben **Kurzname**, "C", das Standard-Präfix für einen Klassennamen vorangestellt.  
  
 **.h-Datei**  
 Legt den Namen der Headerdatei für die neue Klasse des Objekts. Standardmäßig basiert auf den Namen, die Sie, in angeben diesen Namen **Kurzname**. Klicken Sie auf die Schaltfläche mit den Auslassungspunkten, um den Dateinamen an den Speicherort Ihrer Wahl speichern oder die Klassendeklaration an eine vorhandene Datei anfügen. Wenn Sie eine vorhandene Datei auswählen, der Assistent wird nicht zum Speichern an den ausgewählten Speicherort bis auf **Fertig stellen** im Assistenten.  
  
 Der Assistent überschreibt eine Datei nicht. Wenn Sie den Namen einer vorhandenen Datei auswählen, wenn Sie auf **Fertig stellen**, werden vom Assistenten aufgefordert, um anzugeben, ob die Klassendeklaration an den Inhalt der Datei angefügt werden sollen. Klicken Sie auf **Ja** anzufügende Datei ein, klicken Sie auf **keine** zum Assistenten zurückzukehren, und geben Sie einen anderen Dateinamen an.  
  
 **CPP-Datei**  
 Legt den Namen der Implementierungsdatei für das neue Objekt-Klasse. Standardmäßig basiert auf den Namen, die Sie, in angeben diesen Namen **Kurzname**. Klicken Sie auf die Schaltfläche mit den Auslassungspunkten, um den Dateinamen am Speicherort Ihrer Wahl zu speichern. Die Datei wird nicht an den ausgewählten Speicherort gespeichert, bis Sie auf **Fertig stellen** im Assistenten.  
  
 Der Assistent überschreibt eine Datei nicht. Wenn Sie den Namen einer vorhandenen Datei auswählen, wenn Sie auf **Fertig stellen**, werden vom Assistenten aufgefordert, um anzugeben, ob die Implementierung der Klasse mit dem Inhalt der Datei angefügt werden sollen. Klicken Sie auf **Ja** anzufügende Datei ein, klicken Sie auf **keine** zum Assistenten zurückzukehren, und geben Sie einen anderen Dateinamen an.  
  
## <a name="see-also"></a>Siehe auch  
 [ATL-Dialogfeld](../../atl/reference/adding-an-atl-dialog-box.md)
