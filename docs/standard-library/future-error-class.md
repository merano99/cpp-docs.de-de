---
title: future_error-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: future/std::future_error
dev_langs: C++
ms.assetid: 6071c545-ac2a-49ef-9967-07b0125da861
caps.latest.revision: "13"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: cdb482dd71e19ad784e0e878432d800a384d57fa
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="futureerror-class"></a>future_error-Klasse
Beschreibt ein Ausnahmeobjekt, das von Methoden der Typen ausgelöst werden kann, die [future](../standard-library/future-class.md)-Objekte verwalten.  
  
## <a name="syntax"></a>Syntax  
  
```
class future_error : public logic_error {
public:
    future_error(error_code code);

const error_code& code() const throw();

const char *what() const throw();

};
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<zukünftige >  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [Headerdateienreferenz](../standard-library/cpp-standard-library-header-files.md)   
 [logic_error-Klasse](../standard-library/logic-error-class.md)   
 [error_code-Klasse](../standard-library/error-code-class.md)