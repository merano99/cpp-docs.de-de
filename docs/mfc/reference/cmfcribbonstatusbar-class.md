---
title: CMFCRibbonStatusBar-Klasse
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonStatusBar
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddDynamicElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddExtendedElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddSeparator
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::Create
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::CreateEx
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::FindByID
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::FindElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetCount
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetExCount
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetExElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetExtendedArea
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetSpace
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::IsBottomFrame
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::IsExtendedElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::IsInformationMode
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::RecalcLayout
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::RemoveAll
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::RemoveElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::SetInformation
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::OnDrawInformation
helpviewer_keywords:
- CMFCRibbonStatusBar [MFC], AddDynamicElement
- CMFCRibbonStatusBar [MFC], AddElement
- CMFCRibbonStatusBar [MFC], AddExtendedElement
- CMFCRibbonStatusBar [MFC], AddSeparator
- CMFCRibbonStatusBar [MFC], Create
- CMFCRibbonStatusBar [MFC], CreateEx
- CMFCRibbonStatusBar [MFC], FindByID
- CMFCRibbonStatusBar [MFC], FindElement
- CMFCRibbonStatusBar [MFC], GetCount
- CMFCRibbonStatusBar [MFC], GetElement
- CMFCRibbonStatusBar [MFC], GetExCount
- CMFCRibbonStatusBar [MFC], GetExElement
- CMFCRibbonStatusBar [MFC], GetExtendedArea
- CMFCRibbonStatusBar [MFC], GetSpace
- CMFCRibbonStatusBar [MFC], IsBottomFrame
- CMFCRibbonStatusBar [MFC], IsExtendedElement
- CMFCRibbonStatusBar [MFC], IsInformationMode
- CMFCRibbonStatusBar [MFC], RecalcLayout
- CMFCRibbonStatusBar [MFC], RemoveAll
- CMFCRibbonStatusBar [MFC], RemoveElement
- CMFCRibbonStatusBar [MFC], SetInformation
- CMFCRibbonStatusBar [MFC], OnDrawInformation
ms.assetid: 921eb57f-3b40-49fa-a38c-3f2fb6dc2893
ms.openlocfilehash: 068cff9ea3827e780bec886bc5d4b0e263c02e62
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50635343"
---
# <a name="cmfcribbonstatusbar-class"></a>CMFCRibbonStatusBar-Klasse

Die `CMFCRibbonStatusBar` -Klasse implementiert ein Statusleisten-Steuerelement, das Menübandelemente anzeigen kann.

## <a name="syntax"></a>Syntax

```
class CMFCRibbonStatusBar : public CMFCRibbonBar
```

## <a name="members"></a>Member

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|[CMFCRibbonStatusBar::AddDynamicElement](#adddynamicelement)|Die Menüband-Statusleiste wird ein dynamisches Element hinzugefügt.|
|[CMFCRibbonStatusBar::AddElement](#addelement)|Die Menüband-Statusleiste wird ein neues Menübandelement hinzugefügt.|
|[CMFCRibbonStatusBar::AddExtendedElement](#addextendedelement)|Fügt ein Menübandelement zu erweiterten Bereich des Status-Menübands.|
|[CMFCRibbonStatusBar::AddSeparator](#addseparator)|Eine Trennzeichen und der Menüband-Statusleiste hinzugefügt.|
|[CMFCRibbonStatusBar::Create](#create)|Erstellt eine Menüband-Statusleiste an.|
|[CMFCRibbonStatusBar::CreateEx](#createex)|Erstellt eine Menüband-Statusleiste mit einem erweiterten Format an.|
|[CMFCRibbonStatusBar::FindByID](#findbyid)||
|[CMFCRibbonStatusBar::FindElement](#findelement)|Gibt einen Zeiger auf das Element mit der angegebenen Befehls-ID.|
|[CMFCRibbonStatusBar::GetCount](#getcount)|Gibt die Anzahl von Elementen, die im Hauptbereich des Status-Menübands befinden.|
|[CMFCRibbonStatusBar::GetElement](#getelement)|Gibt einen Zeiger auf das Element, das sich am angegebenen Index befindet.|
|[CMFCRibbonStatusBar::GetExCount](#getexcount)|Gibt die Anzahl von Elementen, die im erweiterten Bereich des Status-Menübands befinden.|
|[CMFCRibbonStatusBar::GetExElement](#getexelement)|Gibt einen Zeiger auf das Element zurück, das sich an einem angegebenen Index im erweiterten Bereich des Status-Menübands befindet.|
|[CMFCRibbonStatusBar::GetExtendedArea](#getextendedarea)||
|[CMFCRibbonStatusBar::GetSpace](#getspace)||
|[CMFCRibbonStatusBar::IsBottomFrame](#isbottomframe)||
|[CMFCRibbonStatusBar::IsExtendedElement](#isextendedelement)||
|[CMFCRibbonStatusBar::IsInformationMode](#isinformationmode)|Bestimmt, ob die Informationen im Modus für die Status-Menübands aktiviert ist.|
|[CMFCRibbonStatusBar::RecalcLayout](#recalclayout)|(Überschreibt [CMFCRibbonBar::RecalcLayout](../../mfc/reference/cmfcribbonbar-class.md#recalclayout).)|
|[CMFCRibbonStatusBar::RemoveAll](#removeall)|Entfernt alle Elemente in der Menüband-Statusleiste.|
|[CMFCRibbonStatusBar::RemoveElement](#removeelement)|Entfernt das Element, das eine angegebene Befehls-ID in der Menüband-Statusleiste verfügt.|
|[CMFCRibbonStatusBar::SetInformation](#setinformation)|Aktiviert oder deaktiviert den Modus der Informationen für die Menüband-Statusleiste.|

### <a name="protected-methods"></a>Geschützte Methoden

|Name|Beschreibung|
|----------|-----------------|
|[CMFCRibbonStatusBar::OnDrawInformation](#ondrawinformation)|Zeigt die Zeichenfolge, die angezeigt wird, klicken Sie auf der Menüband-Statusleiste angezeigt, wenn die Informationen im Modus aktiviert ist.|

## <a name="remarks"></a>Hinweise

Benutzer können die Sichtbarkeit von Menübandelementen auf einem Menüband-Statusleiste mithilfe der integrierten Kontextmenü für die Menüband-Statusleiste ändern. Sie können die hinzufügen oder entfernen Sie die Elemente dynamisch.

Eine Menüband-Statusleiste enthält zwei Bereiche: einen Hauptbereich und einen erweiterten Bereich. Der erweiterte Bereich auf der rechten Seite des Status-Menübands angezeigt wird und in einer anderen Farbe angezeigt wird, als der wichtigste Bereich ist.

In der Regel der Hauptbereich der Statusleiste zeigt Benachrichtigungen und erweiterte Bereich werden Steuerelemente angezeigt. Der erweiterte Bereich bleibt so lange wie möglich sichtbar, wenn der Benutzer die Größe die Menüband-Statusleiste ändert.

## <a name="example"></a>Beispiel

Das folgende Beispiel veranschaulicht die Verwendung verschiedener Methoden in der `CMFCRibbonStatusBar` -Klasse. Das Beispiel zeigt, wie Sie ein neues Menübandelement um Status-Menübands hinzufügen, fügen ein Menübandelement hinzu erweiterten Bereich des Status-Menübands, fügen Sie ein Trennzeichen hinzu, und aktivieren Sie den normalen Modus für die Menüband-Statusleiste.

[!code-cpp[NVC_MFC_RibbonApp#15](../../mfc/reference/codesnippet/cpp/cmfcribbonstatusbar-class_1.cpp)]
[!code-cpp[NVC_MFC_RibbonApp#16](../../mfc/reference/codesnippet/cpp/cmfcribbonstatusbar-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)

[CMFCRibbonStatusBar](../../mfc/reference/cmfcribbonstatusbar-class.md)

## <a name="requirements"></a>Anforderungen

**Header:** afxribbonstatusbar.h

##  <a name="adddynamicelement"></a>  CMFCRibbonStatusBar::AddDynamicElement

Die Menüband-Statusleiste wird ein dynamisches Element hinzugefügt.

```
void AddDynamicElement(CMFCRibbonBaseElement* pElement);
```

### <a name="parameters"></a>Parameter

*pElement*<br/>
[in] Ein Zeiger auf ein dynamisches Element.

### <a name="remarks"></a>Hinweise

Im Gegensatz zu regulären Elementen dynamischen Elemente sind nicht anpassbar, und klicken Sie im Menü "anpassen" der Statusleiste nicht angezeigt.

##  <a name="addelement"></a>  CMFCRibbonStatusBar::AddElement

Die Menüband-Statusleiste wird ein neues Menübandelement hinzugefügt.

```
void AddElement(
    CMFCRibbonBaseElement* pElement,
    LPCTSTR lpszLabel,
    BOOL bIsVisible=TRUE);
```

### <a name="parameters"></a>Parameter

*pElement*<br/>
[in] Ein Zeiger auf das hinzugefügte Element.

*lpszLabel*<br/>
[in] Eine Beschriftung des Elements.

*bIsVisible*<br/>
[in] TRUE, wenn Sie das Element als sichtbar ist, "false" hinzufügen möchten, wenn Sie das Element als ausgeblendet hinzufügen möchten.

##  <a name="addextendedelement"></a>  CMFCRibbonStatusBar::AddExtendedElement

Fügt ein Menübandelement zu erweiterten Bereich des Status-Menübands.

```
void AddExtendedElement(
    CMFCRibbonBaseElement* pElement,
    LPCTSTR lpszLabel,
    BOOL bIsVisible=TRUE);
```

### <a name="parameters"></a>Parameter

*pElement*<br/>
[in] Ein Zeiger auf das hinzugefügte Element.

*lpszLabel*<br/>
[in] Die textbezeichnung des Elements.

*bIsVisible*<br/>
[in] TRUE, wenn Sie das Element als sichtbar ist, "false" hinzufügen möchten, wenn Sie das Element als ausgeblendet hinzufügen möchten.

### <a name="remarks"></a>Hinweise

Der erweiterte Bereich befindet sich rechts vom Statusleisten-Steuerelement.

##  <a name="addseparator"></a>  CMFCRibbonStatusBar::AddSeparator

Eine Trennzeichen und der Menüband-Statusleiste hinzugefügt.

```
void AddSeparator();
```

### <a name="remarks"></a>Hinweise

Das Framework Fügt ein Trennzeichen nach der Methode [CMFCRibbonStatusBar::AddElement](#addelement). Fügt das letzte Element.

##  <a name="create"></a>  CMFCRibbonStatusBar::Create

Erstellt eine Menüband-Statusleiste an.

```
BOOL Create(
    CWnd* pParentWnd,
    DWORD dwStyle=WS_CHILD|WS_VISIBLE|CBRS_BOTTOM,
    UINT nID=AFX_IDW_STATUS_BAR);
```

### <a name="parameters"></a>Parameter

*pParentWnd*<br/>
[in] Ein Zeiger auf das übergeordnete Fenster.

*dwStyle*<br/>
[in] Eine logische OR-Kombination der Stile von Listensteuerelementen.

*nID*<br/>
[in] Die Steuerelement-ID der Statusleiste.

### <a name="return-value"></a>Rückgabewert

TRUE, wenn "false" auf die Statusleiste erfolgreich, andernfalls erstellt wird.

##  <a name="createex"></a>  CMFCRibbonStatusBar::CreateEx

Erstellt eine Menüband-Statusleiste, die über einen erweiterten Stil verfügt.

```
BOOL CreateEx(
    CWnd* pParentWnd,
    DWORD dwCtrlStyle=0,
    DWORD dwStyle=WS_CHILD|WS_VISIBLE|CBRS_BOTTOM,
    UINT nID=AFX_IDW_STATUS_BAR);
```

### <a name="parameters"></a>Parameter

*pParentWnd*<br/>
Ein Zeiger auf das übergeordnete Fenster.

*dwCtrlStyle*<br/>
Eine logische OR-Kombination der zusätzliche Formate für das Status-Bar-Objekt erstellen.

*dwStyle*<br/>
Das Format des Steuerelements der Statusleiste.

*nID*<br/>
Die Steuerelement-ID der Statusleiste.

### <a name="return-value"></a>Rückgabewert

TRUE, wenn "false" auf die Statusleiste erfolgreich, andernfalls erstellt wird.

##  <a name="findbyid"></a>  CMFCRibbonStatusBar::FindByID

Weitere Informationen finden Sie im Quellcode der **VC\\Atlmfc\\Src\\Mfc** Ordner von Visual Studio-Installation.

```
CMFCRibbonBaseElement* FindByID(UINT uiCmdID, BOOL = TRUE);
```

### <a name="parameters"></a>Parameter

[in] *UiCmdID*<br/>
[in] *"Bool"*<br/>

### <a name="return-value"></a>Rückgabewert

### <a name="remarks"></a>Hinweise

##  <a name="findelement"></a>  CMFCRibbonStatusBar::FindElement

Gibt einen Zeiger auf das Element mit der angegebenen Befehls-ID.

```
CMFCRibbonBaseElement* FindElement(UINT uiID);
```

### <a name="parameters"></a>Parameter

*uiID*<br/>
[in] Die ID des Elements.

### <a name="return-value"></a>Rückgabewert

Ein Zeiger auf das Element mit der angegebenen Befehls-ID. NULL, wenn kein solches Element vorhanden ist.

##  <a name="getcount"></a>  CMFCRibbonStatusBar::GetCount

Gibt die Anzahl von Elementen, die im Hauptbereich des Status-Menübands befinden.

```
int GetCount() const;
```

### <a name="return-value"></a>Rückgabewert

Die Anzahl der Elemente, die im Hauptbereich des Status-Menübands befinden.

##  <a name="getelement"></a>  CMFCRibbonStatusBar::GetElement

Gibt einen Zeiger auf das Element, das sich am angegebenen Index befindet.

```
CMFCRibbonBaseElement* GetElement(int nIndex);
```

### <a name="parameters"></a>Parameter

*nIndex*<br/>
[in] Gibt einen nullbasierten Index eines Elements, das im Hauptbereich des das StatusBar-Steuerelement befindet.

### <a name="return-value"></a>Rückgabewert

Ein Zeiger auf das Element, das sich am angegebenen Index befindet. NULL, wenn der Index negativ ist oder die Anzahl der Elemente in der Statusleiste angezeigt überschreitet.

### <a name="remarks"></a>Hinweise

##  <a name="getexcount"></a>  CMFCRibbonStatusBar::GetExCount

Gibt die Anzahl von Elementen, die im erweiterten Bereich des Status-Menübands befinden.

```
int GetExCount() const;
```

### <a name="return-value"></a>Rückgabewert

Die Anzahl der Elemente, die im erweiterten Bereich des Status-Menübands befinden.

##  <a name="getexelement"></a>  CMFCRibbonStatusBar::GetExElement

Gibt einen Zeiger auf das Element zurück, das sich an einem angegebenen Index im erweiterten Bereich des Status-Menübands befindet. Der erweiterte Bereich befindet sich rechts vom Statusleisten-Steuerelement.

```
CMFCRibbonBaseElement* GetExElement(int nIndex);
```

### <a name="parameters"></a>Parameter

*nIndex*<br/>
[in] Gibt den nullbasierten Index eines Elements, das im erweiterten Bereich des das StatusBar-Steuerelement befindet.

### <a name="return-value"></a>Rückgabewert

Ein Zeiger auf das Element, das sich an einem angegebenen Index im erweiterten Bereich des Status-Menübands befindet. NULL, wenn *nIndex* ist negativ oder überschreitet die Anzahl der Elemente im erweiterten Bereich des Status-Menübands.

### <a name="remarks"></a>Hinweise

##  <a name="getextendedarea"></a>  CMFCRibbonStatusBar::GetExtendedArea

Weitere Informationen finden Sie im Quellcode der **VC\\Atlmfc\\Src\\Mfc** Ordner von Visual Studio-Installation.

```
virtual BOOL GetExtendedArea(CRect& rect) const;
```

### <a name="parameters"></a>Parameter

[in] *Rect*<br/>

### <a name="return-value"></a>Rückgabewert

### <a name="remarks"></a>Hinweise

##  <a name="getspace"></a>  CMFCRibbonStatusBar::GetSpace

Weitere Informationen finden Sie im Quellcode der **VC\\Atlmfc\\Src\\Mfc** Ordner von Visual Studio-Installation.

```
int GetSpace() const;
```

### <a name="return-value"></a>Rückgabewert

### <a name="remarks"></a>Hinweise

##  <a name="isbottomframe"></a>  CMFCRibbonStatusBar::IsBottomFrame

Weitere Informationen finden Sie im Quellcode der **VC\\Atlmfc\\Src\\Mfc** Ordner von Visual Studio-Installation.

```
BOOL IsBottomFrame() const;
```

### <a name="return-value"></a>Rückgabewert

### <a name="remarks"></a>Hinweise

##  <a name="isextendedelement"></a>  CMFCRibbonStatusBar::IsExtendedElement

Weitere Informationen finden Sie im Quellcode der **VC\\Atlmfc\\Src\\Mfc** Ordner von Visual Studio-Installation.

```
BOOL IsExtendedElement(CMFCRibbonBaseElement* pElement) const;
```

### <a name="parameters"></a>Parameter

[in] *pElement*<br/>

### <a name="return-value"></a>Rückgabewert

### <a name="remarks"></a>Hinweise

##  <a name="isinformationmode"></a>  CMFCRibbonStatusBar::IsInformationMode

Bestimmt, ob die Informationen im Modus für die Status-Menübands aktiviert ist.

```
BOOL IsInformationMode() const;
```

### <a name="return-value"></a>Rückgabewert

True, wenn die Statusleiste im Informationen Modus arbeiten kann. andernfalls "false".

### <a name="remarks"></a>Hinweise

Im Modus "Informationen" die Statusleiste Blendet alle regulären Bereiche und zeigt eine Meldungszeichenfolge.

##  <a name="ondrawinformation"></a>  CMFCRibbonStatusBar::OnDrawInformation

Zeigt die Zeichenfolge, die angezeigt wird, in der Menüband-Statusleiste angezeigt, wenn die Informationen im Modus aktiviert ist.

```
virtual void OnDrawInformation(
    CDC* pDC,
    CString& strInfo,
    CRect rectInfo);
```

### <a name="parameters"></a>Parameter

*pDC*<br/>
[in] Ein Zeiger auf einen Gerätekontext.

*strInfo*<br/>
[in] Die Informationszeichenfolge.

*rectInfo*<br/>
[in] Das umschließende Rechteck.

### <a name="remarks"></a>Hinweise

Überschreiben Sie diese Methode in einer abgeleiteten Klasse, wenn Sie die Darstellung der Zeichenfolge in der Statusleiste anpassen möchten. Verwenden der [CMFCRibbonStatusBar::SetInformation](#setinformation) Methode, um die Statusleiste in den Informationen im Modus versetzen. In diesem Modus wird die Statusleiste Blendet alle Bereiche und zeigt die Informationszeichenfolge gemäß *StrInfo*.

##  <a name="recalclayout"></a>  CMFCRibbonStatusBar::RecalcLayout

Weitere Informationen finden Sie im Quellcode der **VC\\Atlmfc\\Src\\Mfc** Ordner von Visual Studio-Installation.

```
virtual void RecalcLayout();
```

### <a name="remarks"></a>Hinweise

##  <a name="removeall"></a>  CMFCRibbonStatusBar::RemoveAll

Entfernt alle Elemente in der Menüband-Statusleiste.

```
void RemoveAll();
```

##  <a name="removeelement"></a>  CMFCRibbonStatusBar::RemoveElement

Entfernt das Element, das eine angegebene Befehls-ID in der Menüband-Statusleiste verfügt.

```
BOOL RemoveElement(UINT uiID);
```

### <a name="parameters"></a>Parameter

*uiID*<br/>
[in] Die ID des Elements in der Statusleiste zu entfernen.

### <a name="return-value"></a>Rückgabewert

TRUE, wenn ein Element mit dem angegebenen *UiID* wird entfernt. "False" andernfalls.

##  <a name="setinformation"></a>  CMFCRibbonStatusBar::SetInformation

Aktiviert oder deaktiviert den Modus der Informationen für die Menüband-Statusleiste.

```
void SetInformation(LPCTSTR lpszInfo);
```

### <a name="parameters"></a>Parameter

*lpszInfo*<br/>
[in] Die Informationszeichenfolge.

### <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um die Statusleiste in den Modus für die Informationen zu platzieren. In diesem Modus wird die Statusleiste Blendet alle Bereiche und zeigt die Informationszeichenfolge gemäß *LpszInfo*.

Wenn LpszInfo NULL ist, wird die Statusleiste zum normalen Modus zurückgesetzt.

## <a name="see-also"></a>Siehe auch

[Hierarchiediagramm](../../mfc/hierarchy-chart.md)<br/>
[Klassen](../../mfc/reference/mfc-classes.md)<br/>
[CMFCRibbonBar-Klasse](../../mfc/reference/cmfcribbonbar-class.md)<br/>
[CMFCRibbonBaseElement-Klasse](../../mfc/reference/cmfcribbonbaseelement-class.md)<br/>
[CMFCRibbonBar-Klasse](../../mfc/reference/cmfcribbonbar-class.md)
