---
title: time_put_byname-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- xloctime/std::time_put_byname
dev_langs:
- C++
helpviewer_keywords:
- time_put_byname class
ms.assetid: e08c2348-64d2-4ace-98b1-1496e14c7b1a
caps.latest.revision: 25
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 65f4e356ad0d46333b0d443d0fd6ac0b9f2b6f58
ms.openlocfilehash: ba50414643d430798912e6a7a25d3fe9c49c1b9a
ms.contentlocale: de-de
ms.lasthandoff: 10/03/2017

---
# <a name="timeputbyname-class"></a>time_put_byname-Klasse
Diese abgeleitete Vorlagenklasse beschreibt ein Objekt, das als Gebietsschemafacet vom Typ `time_put`\< CharType, OutputIterator > dienen kann.  
  
## <a name="syntax"></a>Syntax  
  
```
template <class CharType, class OutIt = ostreambuf_iterator<CharType, char_traits<CharType>>>
class time_put_byname : public time_put<CharType, OutputIterator>
{
public:
    explicit time_put_byname(
    const char* _Locname,
    size_t _Refs = 0);

    explicit time_put_byname(
    const string& _Locname,
    size_t _Refs = 0);

protected:
    virtual ~time_put_byname();

};
```  
  
#### <a name="parameters"></a>Parameter  
 `_Locname`  
 Name eines Gebietsschemas.  
  
 `_Refs`  
 Eine initiale Verweisanzahl.  
  
## <a name="remarks"></a>Hinweise  
 Das Verhalten wird durch das [named](../standard-library/locale-class.md#name)-Gebietsschema `_Locname` bestimmt. Alle Konstruktoren initialisieren ihr jeweiliges Basisobjekt mit [time_put](../standard-library/time-put-class.md#time_put)\<CharType, OutputIterator>( `_Refs`).  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<locale>  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [Threadsicherheit in der C++-Standardbibliothek](../standard-library/thread-safety-in-the-cpp-standard-library.md)



