---
title: 'Platform:: recreateexception-Methode | Microsoft Docs'
ms.custom: 
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: VCCORLIB/Platform::Exception
dev_langs: C++
helpviewer_keywords: Platform::Exception Class
ms.assetid: fa73d1ab-86e4-4d26-a7d9-81938c1c7e77
caps.latest.revision: "6"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.openlocfilehash: e617d85c17db3c1e3cccb64786dfe7bfcfb9b1e6
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="platformrecreateexception-method"></a>Platform::ReCreateException-Methode
Diese Methode ist nur für die interne Verwendung bestimmt und nicht für Benutzercode gedacht. Verwenden Sie stattdessen die Exception:: createexception-Methode.

## <a name="syntax"></a>Syntax

```cpp
static Exception^ ReCreateException(int hr)
```

### <a name="parameters"></a>Parameter
`hr`

### <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt eine neue Platform::Exception^ basierend auf dem angegebenen HRESULT zurück.
