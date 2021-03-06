---
title: CSession-Klasse
ms.date: 11/04/2016
f1_keywords:
- CSession
- ATL::CSession
- ATL.CSession
- CSession.Abort
- CSession::Abort
- ATL.CSession.Abort
- ATL::CSession::Abort
- CSession::Close
- ATL.CSession.Close
- CSession.Close
- ATL::CSession::Close
- CSession.Commit
- ATL.CSession.Commit
- ATL::CSession::Commit
- CSession::Commit
- GetTransactionInfo
- CSession.GetTransactionInfo
- ATL.CSession.GetTransactionInfo
- CSession::GetTransactionInfo
- ATL::CSession::GetTransactionInfo
- ATL::CSession::Open
- CSession::Open
- CSession.Open
- ATL.CSession.Open
- CSession::StartTransaction
- StartTransaction
- ATL.CSession.StartTransaction
- CSession.StartTransaction
- ATL::CSession::StartTransaction
helpviewer_keywords:
- CSession class
- Abort method
- Close method
- Commit method
- GetTransactionInfo method
- Open method
- StartTransaction method
ms.assetid: 83cd798f-b45d-4f11-a23c-29183390450c
ms.openlocfilehash: f3b77823608376fdfc12beacf7cab5dd810c415e
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556789"
---
# <a name="csession-class"></a>CSession-Klasse

Stellt eine einzelne Datenbank-Access-Sitzung dar.

## <a name="syntax"></a>Syntax

```cpp
class CSession
```

## <a name="requirements"></a>Anforderungen

**Header:** atldbcli.h

## <a name="members"></a>Member

### <a name="methods"></a>Methoden

|||
|-|-|
|[Abort](#abort)|Abgebrochen (beendet) der Transaktion.|
|[Schließen](#close)|Schließt die Sitzung.|
|[Commit](#commit)|Führt einen Commit die Transaktion.|
|[GetTransactionInfo](#gettransactioninfo)|Gibt Informationen zu einer Transaktion zurück.|
|[Öffnen](#open)|Öffnet eine neue Sitzung für das Datenquellenobjekt.|
|[StartTransaction](#starttransaction)|Startet eine neue Transaktion für diese Sitzung.|

## <a name="remarks"></a>Hinweise

Eine oder mehrere Sitzungen können zugeordnet werden, mit jeder anbieterverbindung (Datenquelle), der durch dargestellt wird ein [CDataSource](../../data/oledb/cdatasource-class.md) Objekt. Zum Erstellen eines neuen `CSession` für eine `CDataSource`, rufen Sie [CSession:: Open](../../data/oledb/csession-open.md). Zum Starten einer Datenbanktransaktion `CSession` bietet die `StartTransaction` Methode. Sobald eine Transaktion gestartet wird, Sie können einen commit mithilfe der `Commit` -Methode, oder brechen Sie den Befehl mit der `Abort` Methode.

## <a name="abort"></a> CSession:: Abort

Wird die Transaktion beendet.

### <a name="syntax"></a>Syntax

```cpp
HRESULT Abort(BOID* pboidReason = NULL,
   BOOL bRetaining = FALSE,
   BOOL bAsync = FALSE) const throw();
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [ITransaction:: Abort](https://docs.microsoft.com/previous-versions/windows/desktop/ms709833(v=vs.85)) in die *OLE DB-Programmierreferenz*.

### <a name="return-value"></a>Rückgabewert

Ein standard-HRESULT.

## <a name="close"></a> CSession:: Close

Schließt die Sitzung, die von geöffnet wurde [CSession:: Open](../../data/oledb/csession-open.md).

### <a name="syntax"></a>Syntax

```cpp
void Close() throw();
```

### <a name="remarks"></a>Hinweise

Versionen der `m_spOpenRowset` Zeiger.

## <a name="commit"></a> CSession:: Commit

Führt einen Commit die Transaktion.

### <a name="syntax"></a>Syntax

```cpp
HRESULT Commit(BOOL bRetaining = FALSE,
   DWORD grfTC = XACTTC_SYNC,
   DWORD grfRM = 0) const throw();
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [ITransaction:: Commit](https://docs.microsoft.com/previous-versions/windows/desktop/ms713008(v=vs.85)) in die *OLE DB-Programmierreferenz*.

### <a name="return-value"></a>Rückgabewert

Ein standard-HRESULT.

### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [ITransaction:: Commit](https://docs.microsoft.com/previous-versions/windows/desktop/ms713008(v=vs.85)).

## <a name="gettransactioninfo"></a> CSession:: Gettransactioninfo

Gibt Informationen zu einer Transaktion zurück.

### <a name="syntax"></a>Syntax

```cpp
HRESULT GetTransactionInfo(XACTTRANSINFO* pInfo) const throw();
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [ITransaction::GetTransactionInfo](https://docs.microsoft.com/previous-versions/windows/desktop/ms714975(v=vs.85)) in die *OLE DB-Programmierreferenz*.

### <a name="return-value"></a>Rückgabewert

Ein standard-HRESULT.

### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [ITransaction::GetTransactionInfo](https://docs.microsoft.com/previous-versions/windows/desktop/ms714975(v=vs.85)) in die *OLE DB-Programmierreferenz*.

## <a name="open"></a> CSession:: Open

Öffnet eine neue Sitzung für das Datenquellenobjekt.

### <a name="syntax"></a>Syntax

```cpp
HRESULT Open(const CDataSource& ds,
   DBPROPSET *pPropSet = NULL,
   ULONG ulPropSets = 0) throw();
```

#### <a name="parameters"></a>Parameter

*DS*<br/>
[in] Die Datenquelle für die die Sitzung ist, geöffnet werden.

*pPropSet*<br/>
[in] Ein Zeiger auf ein Array von [DBPROPSET](https://docs.microsoft.com/previous-versions/windows/desktop/ms714367(v=vs.85)) Strukturen, die Eigenschaften und Werte festgelegt werden. Finden Sie unter [Eigenschaftensätze und Eigenschaftengruppen](https://docs.microsoft.com/previous-versions/windows/desktop/ms713696(v=vs.85)) in die *OLE DB-Programmierreferenz* in das Windows SDK.

*ulPropSets*<br/>
[in] Die Anzahl der [DBPROPSET](https://docs.microsoft.com/previous-versions/windows/desktop/ms714367(v=vs.85)) Strukturen zu übergeben, der *DBPROPSET* Argument.

### <a name="return-value"></a>Rückgabewert

Ein standard-HRESULT.

### <a name="remarks"></a>Hinweise

Sie müssen das Datenquellenobjekt mithilfe öffnen [CDataSource:: Open](../../data/oledb/cdatasource-open.md) vor der Übergabe an `CSession::Open`.

## <a name="starttransaction"></a> CSession:: StartTransaction

Startet eine neue Transaktion für diese Sitzung.

### <a name="syntax"></a>Syntax

```cpp
HRESULT StartTransaction(ISOLEVEL isoLevel = ISOLATIONLEVEL_READCOMMITTED,
   ULONG isoFlags = 0,
   ITransactionOptions* pOtherOptions = NULL,
   ULONG* pulTransactionLevel = NULL) const throw();
```

#### <a name="parameters"></a>Parameter

Finden Sie unter [ITransactionLocal:: StartTransaction](https://docs.microsoft.com/previous-versions/windows/desktop/ms709786(v=vs.85)) in die *OLE DB-Programmierreferenz*.

### <a name="return-value"></a>Rückgabewert

Ein standard-HRESULT.

### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [ITransactionLocal:: StartTransaction](https://docs.microsoft.com/previous-versions/windows/desktop/ms709786(v=vs.85)) in die *OLE DB-Programmierreferenz*.

## <a name="see-also"></a>Siehe auch

[CatDB](../../visual-cpp-samples.md)<br/>
[OLE DB-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Referenz der OLE DB-Consumervorlagen](../../data/oledb/ole-db-consumer-templates-reference.md)