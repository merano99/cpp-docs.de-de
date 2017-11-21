---
title: Cancellation_token_source-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- cancellation_token_source
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_source
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_source::cancellation_token_source
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_source::cancel
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_source::create_linked_source
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_source::get_token
dev_langs:
- C++
helpviewer_keywords:
- cancellation_token_source class
ms.assetid: 3548b1a0-12b0-4334-95db-4bf57141c066
caps.latest.revision: 10
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 5faef5bd1be6cc02d6614a6f6193c74167a8ff23
ms.openlocfilehash: f41a4a21af5bc37ab612221152b8311a5a91d914
ms.contentlocale: de-de
ms.lasthandoff: 03/17/2017

---
# <a name="cancellationtokensource-class"></a>cancellation_token_source-Klasse
Mit der `cancellation_token_source` -Klasse kann ein abbrechbarer Vorgang abgebrochen werden.  
  
## <a name="syntax"></a>Syntax  
  
```
class cancellation_token_source;
```  
  
## <a name="members"></a>Mitglieder  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[cancellation_token_source](#ctor)|Überladen. Erstellt eine neue `cancellation_token_source`. Die Quelle kann verwendet werden, um den Abbruch eines abbrechbaren Vorgangs zu kennzeichnen.|  
|[~ Cancellation_token_source-Destruktor](#dtor)||  
  
### <a name="public-methods"></a>Öffentliche Methoden  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[Abbrechen](#cancel)|Bricht das Token ab. Jede `task_group`, `structured_task_group` oder jeder `task`, der das Token nutzt, wird bei diesem Aufruf abgebrochen und löst eine Ausnahme am nächsten Unterbrechungspunkt aus.|  
|[create_linked_source](#create_linked_source)|Überladen. Erstellt eine `cancellation_token_source`, die abgebrochen wird, wenn das bereitgestellte Token abgebrochen wird.|  
|[get_token](#get_token)|Gibt ein Abbruchtoken zurück, das dieser Quelle zugeordnet ist. Das zurückgegebene Token kann für einen Abbruch abgerufen werden oder einen Rückruf bereitstellen, wenn ein Abbruch auftritt.|  
  
### <a name="public-operators"></a>Öffentliche Operatoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[operator!=](#operator_neq)||  
|[operator=](#operator_eq)||  
|[operator==](#operator_eq_eq)||  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 `cancellation_token_source`  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** pplcancellation_token.h  
  
 **Namespace:** Parallelität  
  
##  <a name="dtor"></a>~ Cancellation_token_source 

```
~cancellation_token_source();
```  
  
##  <a name="cancel"></a>Abbrechen 

 Bricht das Token ab. Jede `task_group`, `structured_task_group` oder jeder `task`, der das Token nutzt, wird bei diesem Aufruf abgebrochen und löst eine Ausnahme am nächsten Unterbrechungspunkt aus.  
  
```
void cancel() const;
```  
  
##  <a name="ctor"></a>cancellation_token_source 

 Erstellt eine neue `cancellation_token_source`. Die Quelle kann verwendet werden, um den Abbruch eines abbrechbaren Vorgangs zu kennzeichnen.  
  
```
cancellation_token_source();

cancellation_token_source(const cancellation_token_source& _Src);

cancellation_token_source(cancellation_token_source&& _Src);
```  
  
### <a name="parameters"></a>Parameter  
 `_Src`  
  
##  <a name="create_linked_source"></a>create_linked_source 

 Erstellt eine `cancellation_token_source`, die abgebrochen wird, wenn das bereitgestellte Token abgebrochen wird.  
  
```
static cancellation_token_source create_linked_source(
    cancellation_token& _Src);

template<typename _Iter>
static cancellation_token_source create_linked_source(_Iter _Begin, _Iter _End);
```  
  
### <a name="parameters"></a>Parameter  
 `_Iter`  
 `_Src`  
 Ein Token, dessen Abbruch den Abbruch der zurückgegebenen Tokenquelle verursacht. Beachten Sie, dass die zurückgegebene Tokenquelle auch unabhängig von der Quelle in diesem Parameter abgebrochen werden kann.  
  
 `_Begin`  
 Die C++-Standardbibliothek Iterator am Anfang des tokenbereichs, der auf einen Abbruch überwacht.  
  
 `_End`  
 Die C++-Standardbibliothek Iterator für das Ende des tokenbereichs, der auf einen Abbruch überwacht.  
  
### <a name="return-value"></a>Rückgabewert  
 Eine `cancellation_token_source`, die abgebrochen wird, wenn das vom `_Src`-Parameter bereitgestellte Token abgebrochen wird.  
  
##  <a name="get_token"></a>get_token 

 Gibt ein Abbruchtoken zurück, das dieser Quelle zugeordnet ist. Das zurückgegebene Token kann für einen Abbruch abgerufen werden oder einen Rückruf bereitstellen, wenn ein Abbruch auftritt.  
  
```
cancellation_token get_token() const;
```  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Abbruchtoken, der dieser Quelle zugeordnet ist.  
  
##  <a name="operator_neq"></a>Operator! = 

```
bool operator!= (const cancellation_token_source& _Src) const;
```  
  
### <a name="parameters"></a>Parameter  
 `_Src`  
  
### <a name="return-value"></a>Rückgabewert  
  
##  <a name="operator_eq"></a>Operator = 

```
cancellation_token_source& operator= (const cancellation_token_source& _Src);

cancellation_token_source& operator= (cancellation_token_source&& _Src);
```  
  
### <a name="parameters"></a>Parameter  
 `_Src`  
  
### <a name="return-value"></a>Rückgabewert  
  
##  <a name="operator_eq_eq"></a>Operator == 

```
bool operator== (const cancellation_token_source& _Src) const;
```  
  
### <a name="parameters"></a>Parameter  
 `_Src`  
  
### <a name="return-value"></a>Rückgabewert  
  
## <a name="see-also"></a>Siehe auch  
 [Concurrency-Namespace](concurrency-namespace.md)
