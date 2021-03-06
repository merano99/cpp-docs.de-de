---
title: CMFCRibbonLabel-Klasse
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonLabel
- AFXRIBBONLABEL/CMFCRibbonLabel
- AFXRIBBONLABEL/CMFCRibbonLabel::CMFCRibbonLabel
- AFXRIBBONLABEL/CMFCRibbonLabel::SetACCData
helpviewer_keywords:
- CMFCRibbonLabel [MFC], CMFCRibbonLabel
- CMFCRibbonLabel [MFC], SetACCData
ms.assetid: 0346c891-83bf-4f20-b8a1-c84cf2aadced
ms.openlocfilehash: ae185a81267dce68cda6bc27c5e327b3335a1018
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50436398"
---
# <a name="cmfcribbonlabel-class"></a>CMFCRibbonLabel-Klasse

Implementiert eine nicht anklickbare Bezeichnung für ein Menüband.

## <a name="syntax"></a>Syntax

```
class CMFCRibbonLabel : public CMFCRibbonButton
```

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

|Name|Beschreibung|
|----------|-----------------|
|[CMFCRibbonLabel::CMFCRibbonLabel](#cmfcribbonlabel)|Erstellt und initialisiert ein `CMFCRibbonLabel` Objekt mit der angegebenen Textzeichenfolge.|
|`CMFCRibbonLabel::~CMFCRibbonLabel`|Destruktor.|

### <a name="public-methods"></a>Öffentliche Methoden

|Name|Beschreibung|
|----------|-----------------|
|`CMFCRibbonLabel::CreateObject`|Wird vom Framework verwendet, um eine dynamische Instanz dieses Klassentyps zu erstellen.|
|`CMFCRibbonLabel::GetThisClass`|Durch das Framework verwendet wird, einen Zeiger zum Abrufen der [CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md) -Objekt, das diesem Klassentyp zugeordnet ist.|
|[CMFCRibbonLabel::SetACCData](#setaccdata)|Bestimmt die barrierefreiheitsdaten für das aktuelle Element der Menüband-Bezeichnung an. (Überschreibt [cmfcribbonbutton:: Setaccdata](../../mfc/reference/cmfcribbonbutton-class.md#setaccdata).)|

### <a name="remarks"></a>Hinweise

Nachdem Sie eine Menüband-Bezeichnung erstellt haben, hinzufügen, einen Bereich durch den Aufruf [cmfcribbonpanel:: Add](../../mfc/reference/cmfcribbonpanel-class.md#add).

Sie können keine Menüband-Bezeichnung Symbolleiste für den Schnellzugriff hinzugefügt werden.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonLabel](../../mfc/reference/cmfcribbonlabel-class.md)

## <a name="requirements"></a>Anforderungen

**Header:** afxRibbonLabel.h

##  <a name="cmfcribbonlabel"></a>  CMFCRibbonLabel::CMFCRibbonLabel

Erstellt und initialisiert ein [CMFCRibbonLabel](../../mfc/reference/cmfcribbonlabel-class.md) -Objekt, das zeigt, an der angegebenen Textzeichenfolge.

```
CMFCRibbonLabel(
    LPCTSTR lpszText,
    BOOL bIsMultiLine = FALSE);
```

### <a name="parameters"></a>Parameter

*lpszText*<br/>
[in] Der Text in der Bezeichnung angezeigt werden.

*bIsMultiLine*<br/>
[in] True, um anzugeben, dass die Bezeichnung eine mehrzeilige Bezeichnung ist. andernfalls "false".

##  <a name="setaccdata"></a>  CMFCRibbonLabel::SetACCData

Bestimmt die barrierefreiheitsdaten für das aktuelle Element der Menüband-Bezeichnung an.

```
virtual BOOL SetACCData(
    CWnd* pParent,
    CAccessibilityData& data);
```

### <a name="parameters"></a>Parameter

*pParent*<br/>
[in] Stellt das übergeordnete Fenster des die aktuelle Menüband-Bezeichnung an.

*data*<br/>
[out] Ein Objekt des Typs `CAccessibilityData` , die mit den Zugriff auf Daten des die aktuelle Menüband-Bezeichnung aufgefüllt wird.

### <a name="return-value"></a>Rückgabewert

TRUE, wenn die *Daten* Parameter wurde erfolgreich mit den Zugriff auf Daten des die aktuelle Menüband-Bezeichnung aufgefüllt ist, andernfalls "false".

## <a name="see-also"></a>Siehe auch

[Hierarchiediagramm](../../mfc/hierarchy-chart.md)<br/>
[Klassen](../../mfc/reference/mfc-classes.md)<br/>
[CMFCRibbonButton-Klasse](../../mfc/reference/cmfcribbonbutton-class.md)
