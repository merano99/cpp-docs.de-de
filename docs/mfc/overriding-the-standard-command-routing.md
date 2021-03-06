---
title: Überschreiben des Standardbefehlsroutings
ms.date: 11/04/2016
helpviewer_keywords:
- MFC, command routing
- command routing [MFC], overriding
- command handling [MFC], routing commands
- overriding, standard command routing
ms.assetid: 872b698a-7432-40c4-9008-68721e8effa5
ms.openlocfilehash: 132831939c05f7e8f84c306f5d08bba9cd5e8ea4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50648440"
---
# <a name="overriding-the-standard-command-routing"></a>Überschreiben des Standardbefehlsroutings

In seltenen Fällen, wenn Sie, eine Variation der standard-Framework routing implementieren müssen, können Sie sie überschreiben. Die Idee ist, ändern Sie das routing in eine oder mehrere Klassen, die durch das Überschreiben von `OnCmdMsg` in diesen Klassen. Wenn Sie dies tun:

- In der Klasse, die die Reihenfolge der Übergabe an ein Objekt vom Standard abweichenden beeinträchtigen.

- Neues Objekt in den nicht standardmäßigen oder in Befehlsziele können sie Befehle aus, um wiederum übergeben werden.

Wenn Sie ein neues Objekt in das routing einfügen, muss die Klasse ein Befehlsziel Klasse sein. In der überschreibenden Versionen von `OnCmdMsg`, achten Sie darauf, dass Sie die Version abzurufen, die Sie überschreiben möchten. Finden Sie unter den [OnCmdMsg](../mfc/reference/ccmdtarget-class.md#oncmdmsg) Memberfunktion der Klasse `CCmdTarget` in die *MFC-Referenz* und die Versionen in Klassen wie `CView` und `CDocument` in den angegebenen Quellcode für Beispiele.

## <a name="see-also"></a>Siehe auch

[So ruft das Framework einen Handler auf](../mfc/how-the-framework-calls-a-handler.md)

