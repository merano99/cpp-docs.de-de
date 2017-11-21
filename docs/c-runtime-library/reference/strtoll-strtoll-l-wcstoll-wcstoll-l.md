---
title: strtoll, _strtoll_l, wcstoll, _wcstoll_l | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- strtoll
- wcstoll
- _strtoll_l
- _wcstoll_l
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-convert-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _strtoll_l
- _tcstoll_l
- _tcstoll
- _wcstoll_l
- strtoll
- wcstoll
dev_langs:
- C++
helpviewer_keywords:
- _tcstoll_l function
- _wcstoll_l function
- strtoll function
- wcstoll function
- _tcstoll function
- _strtoll_l function
ms.assetid: e2d05dcf-d3b2-4291-9e60-dee77e540fd7
caps.latest.revision: 5
author: corob-msft
ms.author: corob
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
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: f0e1ad4f2603e055922b2848aacacf65b276bfe0
ms.contentlocale: de-de
ms.lasthandoff: 04/01/2017

---
# <a name="strtoll-strtolll-wcstoll-wcstolll"></a>strtoll, _strtoll_l, wcstoll, _wcstoll_l
Konvertiert eine Zeichenfolge in einen `long long`-Wert.  
  
## <a name="syntax"></a>Syntax  
  
```  
long long strtoll(  
   const char *nptr,  
   char **endptr,  
   int base   
);  
long long wcstoll(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base   
);  
long long _strtoll_l(  
   const char *nptr,  
   char **endptr,  
   int base,  
   _locale_t locale  
);  
long long _wcstoll_l(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base,  
   _locale_t locale  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `nptr`  
 Zu konvertierende mit NULL endende Zeichenfolge.  
  
 `endptr`  
 Zeiger auf das Zeichen, das die Überprüfung stoppt.  
  
 `base`  
 Zu verwendende Zahlenbasis.  
  
 `locale`  
 Das zu verwendende Gebietsschema.  
  
## <a name="return-value"></a>Rückgabewert  
 `strtoll` gibt den in der Zeichenfolge `nptr` dargestellten Wert zurück, es sei denn, die Darstellung würde einen Überlauf verursachen. In diesem Fall wird `LLONG_MAX` oder `LLONG_MIN` zurückgegeben. Die Funktion gibt 0 zurück, wenn keine Konvertierung ausgeführt werden kann. `wcstoll` gibt Werte analog zu `strtoll` zurück.  
  
 `LLONG_MAX` und `LLONG_MIN` werden in LIMITS.H definiert.  
  
 Wenn `nptr``NULL` ist, oder `base` nicht NULL und entweder weniger als 2 oder größer als 36 ist, wird `errno` auf `EINVAL` festgelegt.  
  
 Weitere Informationen zu diesen Fehlercodes finden Sie unter [errno, _doserrno, _sys_errlist und _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).  
  
## <a name="remarks"></a>Hinweise  
 Die `strtoll`-Funktion konvertiert `nptr` in `long long`. Beide Funktionen beenden das Lesen der `nptr`-Zeichenfolge am ersten Zeichen, das nicht als Teil einer Zahl erkannt wird. Dies ist möglicherweise das abschließende NULL-Zeichen, kann aber auch das erste numerische Zeichen sein, das größer oder gleich `base` ist. `wcstoll` ist eine Breitzeichenversion von `strtoll`. Das dazugehörige `nptr`-Argument ist eine Breitzeichenfolge. Ansonsten verhalten sich diese Funktionen identisch.  
  
### <a name="generic-text-routine-mappings"></a>Zuordnung generischer Textroutinen  
  
|TCHAR.H-Routine|_UNICODE und _MBCS nicht definiert.|_MBCS definiert|_UNICODE definiert|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcstoll`|`strtoll`|`strtoll`|`wcstoll`|  
|`_tcstoll_l`|`_strtoll_l`|`_strtoll_l`|`_wcstoll_l`|  
  
 Die `LC_NUMERIC`-Kategorieeinstellung des Gebietsschemas bestimmt das Erkennen des Basiszeichens in `nptr`. Weitere Informationen finden Sie unter [setlocale, _wsetlocale](../../c-runtime-library/reference/setlocale-wsetlocale.md). Die Funktionen ohne das `_l`-Suffix verwenden das aktuelle Gebietsschema. `_strtoll_l` und `_wcstoll_l` sind mit den entsprechenden Funktionen ohne das Suffix nahezu identisch, verwenden jedoch stattdessen das übergebene Gebietsschema. Weitere Informationen finden Sie unter [Locale](../../c-runtime-library/locale.md).  
  
 Wenn `endptr` nicht `NULL` ist, wird ein Zeiger auf das Zeichen, das die Überprüfung beendet hat, an dem Ort gespeichert, der auf `endptr` zeigt. Wenn keine Konvertierung ausgeführt werden kann (keine gültigen Ziffern gefunden oder ungültige Basis angegeben), wird der Wert von `nptr` an dem Speicherort gespeichert, auf den von `endptr` gezeigt wird.  
  
 `strtoll` erwartet, dass `nptr` auf eine Zeichenfolge der folgenden Form zeigt:  
  
 [`whitespace`] [{`+` &#124; `-`}] [`0` [{ `x` &#124; `X` }]] [`digits` &#124; `letters`]  
  
 `whitespace` besteht möglicherweise aus Leerzeichen und Tabulatorzeichen, die ignoriert werden; `digits` sind mindestens eine Dezimalstelle; `letters` sind mindestens ein Buchstabe von "a" bis "z" (oder "A" bis "Z "). Das erste Zeichen, das dieser Form nicht entspricht, beendet die Überprüfung. Wenn `base` zwischen 2 und 36 liegt, wird dieser Wert als Basis der Zahl verwendet. Wenn `base` 0 ist, werden die ersten Zeichen der Zeichenfolge verwendet, auf die von `nptr` gezeigt wird, um die Basis festzulegen. Wenn das erste Zeichen "0 " und das zweite Zeichen nicht "x" oder "X" ist, wird die Zeichenfolge als oktale ganze Zahl interpretiert. Wenn das erste Zeichen "0" und das zweite Zeichen nicht "x" oder "X" ist, wird die Zeichenfolge als hexadezimale ganze Zahl interpretiert. Wenn das erste Zeichen "1" bis "9 " ist, wird die Zeichenfolge als ganze Dezimalzahl interpretiert. Die Buchstaben "a" bis "z" (bzw. "A" bis "Z") werden den Werten 10 bis 35 zugewiesen. Nur Buchstaben, deren zugewiesene Werte kleiner als `base` sind, sind zulässig. Das erste Zeichen außerhalb des Bereichs der Basis beendet die Überprüfung. Wenn beispielsweise `base` 0 und das erste überprüfte Zeichen "0 " sind, wird eine ganze Oktalzahl angenommen und ein "8"- oder "9"- Zeichen beendet die Überprüfung.  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|`strtoll`, `_strtoll_l`|\<stdlib.h>|  
|`wcstoll`, `_wcstoll_l`|\<stdlib.h> oder \<wchar.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Datenkonvertierung](../../c-runtime-library/data-conversion.md)   
 [Locale](../../c-runtime-library/locale.md)   
 [localeconv](../../c-runtime-library/reference/localeconv.md)   
 [setlocale, _wsetlocale](../../c-runtime-library/reference/setlocale-wsetlocale.md)   
 [Funktionen zur Konvertierung von Zeichenfolgen in numerische Werte](../../c-runtime-library/string-to-numeric-value-functions.md)   
 [strtod, _strtod_l, wcstod, _wcstod_l](../../c-runtime-library/reference/strtod-strtod-l-wcstod-wcstod-l.md)   
 [strtol, wcstol, _strtol_l, _wcstol_l](../../c-runtime-library/reference/strtol-wcstol-strtol-l-wcstol-l.md)   
 [strtoul, _strtoul_l, wcstoul, _wcstoul_l](../../c-runtime-library/reference/strtoul-strtoul-l-wcstoul-wcstoul-l.md)   
 [atof, _atof_l, _wtof, _wtof_l](../../c-runtime-library/reference/atof-atof-l-wtof-wtof-l.md)