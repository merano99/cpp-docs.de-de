---
title: Platform::Collections::BackInsertIterator Klasse | Microsoft Docs
ms.custom: 
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: COLLECTION/Platform::Collections::BackInsertIterator::BackInsertIterator
dev_langs: C++
helpviewer_keywords: BackInsertIterator Class
ms.assetid: aecee1ff-100d-4129-b84b-1966f0923dbf
caps.latest.revision: "4"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.openlocfilehash: 197c0c8dc7de6dca562d961635706a51fff992c4
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="platformcollectionsbackinsertiterator-class"></a>Platform::Collections::BackInsertIterator-Klasse
Stellt einen Iterator dar, der Elemente am Ende einer sequenziellen Auflistung einfügt, anstatt sie zu überschreiben.  
  
## <a name="syntax"></a>Syntax  
  
```  
template <typename T>  
class BackInsertIterator : 
public ::std::iterator<::std::output_iterator_tag, void, void, void, void>;  
```  
  
#### <a name="parameters"></a>Parameter  
 `T`  
 Der Elementtyp in der aktuellen Auflistung.  
  
### <a name="remarks"></a>Hinweise  
 Die BackInsertIterator-Klasse implementiert die Regeln, die für die [back_insert_iterator Class](../standard-library/back-insert-iterator-class.md)erforderlich sind.  
  
### <a name="members"></a>Mitglieder  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[Backinsertiterator:: Backinsertiterator](#ctor)|Initialisiert eine neue Instanz der BackInsertIterator-Klasse.|  
  
### <a name="public-operators"></a>Öffentliche Operatoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[BackInsertIterator::operator*-Operator](#operator-dereference)|Ruft einen Verweis auf den aktuellen BackInsertIterator ab.|  
|[BackInsertIterator::operator++-Operator](#operator-increment)|Gibt einen Verweis auf den aktuellen BackInsertIterator zurück. Der Iterator ist unverändert.|  
|[BackInsertIterator::operator=-Operator](#operator-assign)|Fügt das angegebene Objekt am Ende der aktuellen sequenziellen Auflistung an.|  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 `BackInsertIterator`  
  
### <a name="requirements"></a>Anforderungen  
 **Header:** collection.h  
  
 **Namespace:** Platform::Collections  
  
---
## <a name="ctor"></a>Backinsertiterator:: Backinsertiterator-Konstruktor
Initialisiert eine neue Instanz der `BackInsertIterator`-Klasse.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
explicit BackInsertIterator(  
   Windows::Foundation::Collections::IVector<T>^ v);  
```  
  
#### <a name="parameters"></a>Parameter  
 `v`  
 Ein IVector\<T >-Objekt.  
  
### <a name="remarks"></a>Hinweise  
 Ein `BackInsertIterator` fügt Elemente nach dem letzten Element des Objekts ein, das vom Parameter `v` angegeben wird.  
 
## <a name="operator-assign"></a>Backinsertiterator:: Operator =-Operator
Fügt das angegebene Objekt am Ende der aktuellen sequenziellen Auflistung an.  
  
## <a name="syntax"></a>Syntax  
  
```    
BackInsertIterator& operator=( const T& t);  
```  
  
#### <a name="parameters"></a>Parameter  
 `t`  
 Das Objekt, das der aktuellen Auflistung angefügt werden soll.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Verweis auf den aktuellen BackInsertIterator.  

## <a name="operator-dereference"></a>Backinsertiterator:: *-Operator
Ruft einen Verweis auf den aktuellen BackInsertIterator ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
BackInsertIterator& operator*();  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Verweis auf den aktuellen BackInsertIterator.  
  
### <a name="remarks"></a>Hinweise  
 Dieser Operator gibt einen Verweis auf den aktuellen BackInsertIterator zurück; nicht auf ein Element in der aktuellen Sammlung.  
 
## <a name="operator-increment"></a>Backinsertiterator:: Operator++-Operator
Gibt einen Verweis auf den aktuellen BackInsertIterator zurück. Der Iterator ist unverändert.  
  
## <a name="syntax"></a>Syntax  
  
``` 
  
BackInsertIterator& operator++();  
  
BackInsertIterator operator++(int);  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Verweis auf den aktuellen BackInsertIterator.  
  
### <a name="remarks"></a>Hinweise  
 Im ersten Syntaxbeispiel wird der aktuelle BackInsertIterator absichtlich präinkrementiert und in der zweiten Syntax wird der aktuelle BackInsertIterator postinkrementiert. Der Typ `int` in der zweiten Syntax gibt eine Nach-Inkrementierungsoperation an, keinen tatsächlichen ganzzahligen Operanden.  
  
 Dieser Operator ändert jedoch nicht wirklich den BackInsertIterator. Stattdessen gibt dieser Operator einen Verweis auf den unveränderten, aktuellen Iterator zurück. Dies ist das gleiche Verhalten wie [Operator *](#dereference-operator).  
  
  
## <a name="see-also"></a>Siehe auch  
 [Platform-Namespace](platform-namespace-c-cx.md)