---
title: __getmainargs, __wgetmainargs
ms.date: 11/04/2016
apiname:
- __wgetmainargs
- __getmainargs
apilocation:
- msvcr100.dll
- msvcrt.dll
- msvcr110_clr0400.dll
- msvcr80.dll
- msvcr110.dll
- msvcr90.dll
- msvcr120.dll
apitype: DLLExport
f1_keywords:
- __wgetmainargs
- __getmainargs
helpviewer_keywords:
- __wgetmainargs
- __getmainargs
ms.assetid: f72f54eb-9509-4bdf-8752-40fc49055439
ms.openlocfilehash: 6e2bf21f2ac50d3486af56f9581ff6c8d0e0c309
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2018
ms.locfileid: "51523337"
---
# <a name="getmainargs-wgetmainargs"></a>__getmainargs, __wgetmainargs

Ruft die Befehlszeilenanalyse auf und kopiert die Argumente für `main()` zurück durch die übergebenen Zeiger.

## <a name="syntax"></a>Syntax

```cpp
int __getmainargs(
    int * _Argc,
   char *** _Argv,
   char *** _Env,
   int _DoWildCard,
_startupinfo * _StartInfo);

int __wgetmainargs (
   int *_Argc,
   wchar_t ***_Argv,
   wchar_t ***_Env,
   int _DoWildCard,
   _startupinfo * _StartInfo)
```

#### <a name="parameters"></a>Parameter

`_Argc`<br/>
Eine Ganzzahl, die die Anzahl von Argumenten enthält, die in `argv` folgen. Der `argc`-Parameter ist immer größer als oder gleich 1.

`_Argv`<br/>
Ein Array von Zeigern auf Zeichenfolgen, die auf NULL enden und von den Benutzern des Programms eingegebene Befehlszeilenargumente darstellen. Gemäß Konvention ist `argv[0]` der Befehl, mit dem das Programm aufgerufen wird, argv[1] ist das erste Befehlszeilenargument, und so geht es weiter, bis zu argv[argc], das immer **NULL** ist. Das erste Befehlszeilenargument ist immer `argv[1]`, und das letzte ist `argv[argc - 1]`.

`_Env`<br/>
Ein Zeichenfolgenarray, das die Variablen darstellt, die in der Benutzerumgebung festgelegt werden. Das Array wird mit einem **NULL**-Eintrag beendet.

`_DoWildCard`<br/>
Eine ganze Zahl, die, wenn sie auf 1 festgelegt wird, die Platzhalter in den Befehlszeilenargumenten erweitert, oder keine Aktion ausführt, wenn sie auf 0 festgelegt wird.

`_StartInfo`<br/>
Andere Informationen, die an die CRT-DLL übergeben werden.

## <a name="return-value"></a>Rückgabewert

0, wenn erfolgreich; ein negativer Wert, wenn fehlgeschlagen.

## <a name="remarks"></a>Hinweise

Verwenden Sie `__getmainargs` für nicht-Breitzeichen-Plattformen und `__wgetmainargs` für Breitzeichen (Unicode)-Plattformen.

## <a name="requirements"></a>Anforderungen

|-Routine zurückgegebener Wert|Erforderlicher Header|
|-------------|---------------------|
|__getmainargs|internal.h|
|__wgetmainargs|internal.h|