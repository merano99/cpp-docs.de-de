---
title: .FPO
ms.date: 08/30/2018
f1_keywords:
- .FPO
helpviewer_keywords:
- .FPO directive
ms.assetid: 35f4cd61-32f9-4262-b657-73f04f775d09
ms.openlocfilehash: 83d6e81ea7dd35038f27f2721f3cc41fe49ef1bc
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50570503"
---
# <a name="fpo"></a>.FPO

Die. FPO-Richtlinie steuert die Ausgabe der Compilerdiagnose eines Debug-Datensätze zum .debug$ F-Segment oder Abschnitt.

## <a name="syntax"></a>Syntax

> FPO (*CdwLocals*, *CdwParams*, *CbProlog*, *CbRegs*, *fUseBP*,  *CbFrame*)

### <a name="parameters"></a>Parameter

*cdwLocals*<br/>
Die Anzahl der lokalen Variablen, eine vorzeichenlose 32-Bit-Wert.

*cdwParams*<br/>
Die Größe der Parameter in DWORDS, eine vorzeichenlose 16-Bit-Wert.

*cbProlog*<br/>
Anzahl der Bytes im Prolog Funktionscode, eine vorzeichenlose 8-Bit-Wert.

*cbRegs*<br/>
Anzahl der gespeicherten Register.

*fUseBP*<br/>
Gibt an, ob das EBP-Register zugeordnet wurde. 0 oder 1.

*cbFrame*<br/>
Gibt den Rahmentyp.  Finden Sie unter [FPO_DATA](/windows/desktop/api/winnt/ns-winnt-_fpo_data) für Weitere Informationen.

## <a name="see-also"></a>Siehe auch

[Anweisungen – Referenz](../../assembler/masm/directives-reference.md)<br/>