---
title: CD2DPointF-Klasse
ms.date: 11/04/2016
f1_keywords:
- CD2DPointF
- AFXRENDERTARGET/CD2DPointF
- AFXRENDERTARGET/CD2DPointF::CD2DPointF
helpviewer_keywords:
- CD2DPointF [MFC], CD2DPointF
ms.assetid: 30f72083-1c8a-4f50-adb2-72dbbe3522d4
ms.openlocfilehash: 7b9f6634e4b5980d8318557a8822549d226910b5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50559106"
---
# <a name="cd2dpointf-class"></a>CD2DPointF-Klasse

Ein Wrapper für `D2D1_POINT_2F`.

## <a name="syntax"></a>Syntax

```
class CD2DPointF : public D2D1_POINT_2F;
```

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

|Name|Beschreibung|
|----------|-----------------|
|[CD2DPointF::CD2DPointF](#cd2dpointf)|Überladen. Erstellt eine `CD2DPointF` -Sitzungsobjekts `D2D1_POINT_2F` Objekt.|

### <a name="public-operators"></a>Öffentliche Operatoren

|Name|Beschreibung|
|----------|-----------------|
|[CD2DPointF::Operator CPoint](#operator_cpoint)|Konvertiert `CD2DPointF` zu `CPoint` Objekt.|

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`D2D1_POINT_2F`

`CD2DPointF`

## <a name="requirements"></a>Anforderungen

**Header:** afxrendertarget.h

##  <a name="cd2dpointf"></a>  CD2DPointF::CD2DPointF

Erstellt ein Objekt CD2DPointF aus CPoint-Objekt.

```
CD2DPointF(const CPoint& pt);
CD2DPointF(const D2D1_POINT_2F& pt);
CD2DPointF(const D2D1_POINT_2F* pt);
CD2DPointF(FLOAT fX = 0., FLOAT fY = 0.);
```

### <a name="parameters"></a>Parameter

*pt*<br/>
Quellpunkt

*fX*<br/>
X-Quelle

*Anfangsjahr*<br/>
Quelle Y

##  <a name="operator_cpoint"></a>  CD2DPointF::Operator CPoint

CD2DPointF konvertiert in CPoint-Objekt.

```
operator CPoint();
```

### <a name="return-value"></a>Rückgabewert

Aktuelle Wert des D2D an.

## <a name="see-also"></a>Siehe auch

[Klassen](../../mfc/reference/mfc-classes.md)
