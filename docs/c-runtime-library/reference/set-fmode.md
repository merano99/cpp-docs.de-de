---
title: _set_fmode | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: _set_fmode
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
- api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _set_fmode
- set_fmode
dev_langs: C++
helpviewer_keywords:
- file translation [C++], default mode
- _set_fmode function
- file translation [C++], setting mode
- set_fmode function
ms.assetid: f80eb9c7-733b-4652-a9bc-6b3790a35f12
caps.latest.revision: "19"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 317f4ac24d44008f58deeb62e8362b2d09d8309a
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="setfmode"></a>_set_fmode
Legt den Standarddateiübersetzungsmodus für Datei E/A-Vorgänge fest.  
  
## <a name="syntax"></a>Syntax  
  
```  
errno_t _set_fmode(   
   int mode   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in] `mode`  
 Der gewünschte Dateiübersetzungsmodus: `_O_TEXT` oder `_O_BINARY`.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt bei Erfolg 0 bzw. im Fehlerfall einen Fehlercode zurück. Wenn `mode` nicht `_O_TEXT` oder `_O_BINARY` oder `_O_WTEXT` ist, wird der Handler für ungültige Parameter wie in [Parameter Validation (Parameterüberprüfung)](../../c-runtime-library/parameter-validation.md) beschrieben aufgerufen. Wenn die weitere Ausführung zugelassen wird, legt diese Funktion `errno` auf `EINVAL` fest und gibt `EINVAL` zurück.  
  
## <a name="remarks"></a>Hinweise  
 Die Funktion legt die globale Variable [_fmode](../../c-runtime-library/fmode.md) fest. Diese Variable gibt den Standard-Dateiübersetzungsmodus für die Datei-E/A-Vorgänge `_open` und `_pipe` an.  
  
 `_O_TEXT` und `_O_BINARY` werden in Fcntl.h definiert. `EINVAL` wird in Errno.h. definiert.  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|Optionaler Header|  
|-------------|---------------------|---------------------|  
|`_set_fmode`|\<stdlib.h>|\<fcntl.h>, \<errno.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md) in der Einführung.  
  
## <a name="example"></a>Beispiel  
  
```  
// crt_set_fmode.c  
#include <stdlib.h>  
#include <stdio.h>  
#include <fcntl.h>     /* for _O_TEXT and _O_BINARY */  
#include <errno.h>     /* for EINVAL */  
#include <sys\stat.h>  /* for _S_IWRITE */  
#include <share.h>     /* for _SH_DENYNO */  
  
int main()  
{  
   int mode, fd, ret;  
   errno_t err;  
   int buf[12] = { 65, 66, 67, 68, 69, 70, 71, 72, 73, 74,  
                   75, 76 };  
   char * filename = "fmode.out";  
  
   err = _get_fmode(&mode);  
   if (err == EINVAL)  
   {  
      printf( "Invalid parameter: mode\n");  
      return 1;  
   }  
   else  
      printf( "Default Mode is %s\n", mode == _O_TEXT ? "text" :  
              "binary");  
  
   err = _set_fmode(_O_BINARY);  
   if (err == EINVAL)  
   {  
      printf( "Invalid mode.\n");  
      return 1;  
   }  
  
   if ( _sopen_s(&fd, filename, _O_RDWR | _O_CREAT, _SH_DENYNO, _S_IWRITE | _S_IREAD) != 0 )  
   {  
      printf( "Error opening the file %s\n", filename);  
      return 1;  
   }  
  
   if (ret = _write(fd, buf, 12*sizeof(int)) < 12*sizeof(int))  
   {  
      printf( "Problem writing to the file %s.\n", filename);  
      printf( "Number of bytes written: %d\n", ret);  
   }  
  
   if (_close(fd) != 0)  
   {  
      printf("Error closing the file %s. Error code %d.\n",  
             filename, errno);  
   }  
  
   system("type fmode.out");  
}  
```  
  
```Output  
Default Mode is binary  
A   B   C   D   E   F   G   H   I   J   K   L     
```  
  
## <a name="see-also"></a>Siehe auch  
 [_fmode](../../c-runtime-library/fmode.md)   
 [_get_fmode](../../c-runtime-library/reference/get-fmode.md)   
 [_setmode](../../c-runtime-library/reference/setmode.md)   
 [Text- und Binärmodusdatei-E/A](../../c-runtime-library/text-and-binary-mode-file-i-o.md)