---
title: setbuf | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- setbuf
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
- setbuf
dev_langs:
- C++
helpviewer_keywords:
- setbuf function
- stream buffering
ms.assetid: 13beda22-7b56-455d-8a6c-f2eb636885b9
caps.latest.revision: 16
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
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: 2fee25a696156136b7ef61402282a5e22ae31d05
ms.contentlocale: de-de
ms.lasthandoff: 03/29/2017

---
# <a name="setbuf"></a>setbuf
Steuert die Streampufferung. Diese Funktion ist veraltet. Verwenden Sie stattdessen [setvbuf](../../c-runtime-library/reference/setvbuf.md).  
  
## <a name="syntax"></a>Syntax  
  
```  
void setbuf(  
   FILE *stream,  
   char *buffer   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `stream`  
 Zeiger zur `FILE` -Struktur.  
  
 `buffer`  
 Vom Benutzer zugeordneter Speicher.  
  
## <a name="remarks"></a>Hinweise  
 Die `setbuf`-Funktion steuert die Pufferung für `stream`. Das `stream`-Argument muss auf eine offene Datei verweisen, die noch nicht gelesen oder geschrieben wurde. Wenn das `buffer`-Argument `NULL` ist, wird der Stream nicht gepuffert. Wenn dies nicht der Fall ist, muss der Puffer auf ein Zeichenarray der Länge `BUFSIZ` zeigen, wobei `BUFSIZ` die in STDIO.H definierte Puffergröße ist. Für den E/A-Pufferbetrieb wird anstelle des systemseitig für den gegebenen Stream reservierten Puffers der vom Benutzer angegebene Puffer verwendet. Der Stream `stderr` ist standardmäßig ungepuffert, aber Sie können `setbuf` verwenden, um Puffer `stderr` zuzuweisen.  
  
 `setbuf` wurde durch die Routine [setvbuf](../../c-runtime-library/reference/setvbuf.md) ersetzt, die die bevorzugte Routine für neuen Code ist. `setbuf` wird zwecks Kompatibilität mit vorhandenem Code beibehalten.  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|`setbuf`|\<stdio.h>|  
  
 Zusätzliche Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md) in der Einführung.  
  
## <a name="example"></a>Beispiel  
  
```  
// crt_setbuf.c  
// compile with: /W3  
// This program first opens files named DATA1 and  
// DATA2. Then it uses setbuf to give DATA1 a user-assigned  
// buffer and to change DATA2 so that it has no buffer.  
  
#include <stdio.h>  
  
int main( void )  
{  
   char buf[BUFSIZ];  
   FILE *stream1, *stream2;  
  
   fopen_s( &stream1, "data1", "a" );  
   fopen_s( &stream2, "data2", "w" );  
  
   if( (stream1 != NULL) && (stream2 != NULL) )  
   {  
      // "stream1" uses user-assigned buffer:  
      setbuf( stream1, buf ); // C4996  
      // Note: setbuf is deprecated; consider using setvbuf instead  
      printf( "stream1 set to user-defined buffer at: %Fp\n", buf );  
  
      // "stream2" is unbuffered  
      setbuf( stream2, NULL ); // C4996  
      printf( "stream2 buffering disabled\n" );  
      _fcloseall();  
   }  
}  
```  
  
```Output  
stream1 set to user-defined buffer at: 0012FCDC  
stream2 buffering disabled  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Stream-E/A](../../c-runtime-library/stream-i-o.md)   
 [fclose, _fcloseall](../../c-runtime-library/reference/fclose-fcloseall.md)   
 [fflush](../../c-runtime-library/reference/fflush.md)   
 [fopen, _wfopen](../../c-runtime-library/reference/fopen-wfopen.md)   
 [setvbuf](../../c-runtime-library/reference/setvbuf.md)