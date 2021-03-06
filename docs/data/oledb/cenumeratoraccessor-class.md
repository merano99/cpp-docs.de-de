---
title: CEnumeratorAccessor-Klasse
ms.date: 11/04/2016
f1_keywords:
- ATL::CEnumeratorAccessor
- CEnumeratorAccessor
- ATL.CEnumeratorAccessor
- CEnumeratorAccessor.m_bIsParent
- ATL::CEnumeratorAccessor::m_bIsParent
- m_bIsParent
- ATL.CEnumeratorAccessor.m_bIsParent
- CEnumeratorAccessor::m_bIsParent
- ATL::CEnumeratorAccessor::m_nType
- CEnumeratorAccessor.m_nType
- CEnumeratorAccessor::m_nType
- ATL.CEnumeratorAccessor.m_nType
- m_nType
- ATL::CEnumeratorAccessor::m_szDescription
- CEnumeratorAccessor.m_szDescription
- CEnumeratorAccessor::m_szDescription
- ATL.CEnumeratorAccessor.m_szDescription
- CEnumeratorAccessor::m_szName
- ATL.CEnumeratorAccessor.m_szName
- m_szName
- ATL::CEnumeratorAccessor::m_szName
- CEnumeratorAccessor.m_szName
- CEnumeratorAccessor::m_szParseName
- ATL::CEnumeratorAccessor::m_szParseName
- m_szParseName
- CEnumeratorAccessor.m_szParseName
- ATL.CEnumeratorAccessor.m_szParseName
helpviewer_keywords:
- CEnumeratorAccessor class
- m_bIsParent
- m_nType
- m_szDescription
- m_szName
- m_szParseName
ms.assetid: 21e8e7ea-3511-4afe-b33f-d520f4ff82bb
ms.openlocfilehash: 2bcbf55c4bc6d546c8a2b4eca3ea2dbeafc613fa
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556347"
---
# <a name="cenumeratoraccessor-class"></a>CEnumeratorAccessor-Klasse

Ein, die [CEnumerator](../../data/oledb/cenumerator-class.md) Zugriff auf die Daten aus dem Enumerator-Rowset.

## <a name="syntax"></a>Syntax

```cpp
class CEnumeratorAccessor
```

## <a name="requirements"></a>Anforderungen

**Header:** atldbcli.h

## <a name="members"></a>Member

### <a name="data-members"></a>Datenmember

|||
|-|-|
|[m_bIsParent](#bisparent)|Eine Variable, der angibt, ob der Enumerator einen übergeordneten-Enumerator ist die Zeile ist ein Enumerator.|
|[m_nType](#ntype)|Eine Variable, der angibt, ob die Zeile eine Datenquelle oder einen Enumerator beschreibt.|
|[m_szDescription](#szdescription)|Die Beschreibung der Datenquelle oder Enumerator.|
|[m_szName](#szname)|Der Name der Datenquelle oder Enumerator.|
|[m_szParseName](#szparsename)|Zeichenfolge zu übergeben [IParseDisplayName](/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname) einen Moniker für die Datenquelle oder einen Enumerator abrufen.|

## <a name="remarks"></a>Hinweise

Dieses Rowset besteht aus den Datenquellen und Enumeratoren, die der aktuelle Enumerator sichtbar.

## <a name="bisparent"></a> Cenumeratoraccessor:: M_bisparent

Eine Variable, der angibt, ob der Enumerator einen übergeordneten-Enumerator ist die Zeile ist ein Enumerator.

### <a name="syntax"></a>Syntax

```cpp
VARIANT_BOOL m_bIsParent;
```

### <a name="remarks"></a>Hinweise

Finden Sie unter [ISourcesRowset:: GetSourcesRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85)) in die *OLE DB-Programmierreferenz* für Weitere Informationen.

## <a name="ntype"></a> Cenumeratoraccessor:: M_ntype

Eine Variable, der angibt, ob die Zeile eine Datenquelle oder einen Enumerator beschreibt.

### <a name="syntax"></a>Syntax

```cpp
USHORT m_nType;
```

### <a name="remarks"></a>Hinweise

Finden Sie unter [ISourcesRowset:: GetSourcesRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85)) in die *OLE DB-Programmierreferenz* für Weitere Informationen.

## <a name="szdescription"></a> Cenumeratoraccessor:: M_szdescription

Die Beschreibung der Datenquelle oder Enumerator.

### <a name="syntax"></a>Syntax

```cpp
WCHAR m_szDescription[129];
```

### <a name="remarks"></a>Hinweise

Finden Sie unter [ISourcesRowset:: GetSourcesRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85)) in die *OLE DB-Programmierreferenz* für Weitere Informationen.

## <a name="szname"></a> Cenumeratoraccessor:: M_szname

Der Name der Datenquelle oder Enumerator.

### <a name="syntax"></a>Syntax

```cpp
WCHAR m_szName[129];
```

### <a name="remarks"></a>Hinweise

Finden Sie unter [ISourcesRowset:: GetSourcesRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85)) in die *OLE DB-Programmierreferenz* für Weitere Informationen.

## <a name="szparsename"></a> Cenumeratoraccessor:: M_szparsename

Zeichenfolge zu übergeben [IParseDisplayName](/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname) einen Moniker für die Datenquelle oder einen Enumerator abrufen.

### <a name="syntax"></a>Syntax

```cpp
WCHAR m_szParseName[129];
```

### <a name="remarks"></a>Hinweise

Finden Sie unter [ISourcesRowset:: GetSourcesRowset](https://docs.microsoft.com/previous-versions/windows/desktop/ms711200(v=vs.85)) in die *OLE DB-Programmierreferenz* für Weitere Informationen.

## <a name="see-also"></a>Siehe auch

[OLE DB-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Referenz der OLE DB-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-reference.md)