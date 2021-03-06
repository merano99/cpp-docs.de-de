---
title: Überschreiben einer dynamischen Zugriffsmethode
ms.date: 10/19/2018
helpviewer_keywords:
- accessors [C++], dynamic
- dynamic accessors
- overriding, dynamic accessors
ms.assetid: cbefd156-6da5-490d-b795-c2d7d874f7ce
ms.openlocfilehash: 428eeaa61843bbd195de7936656815b5e3c6115f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "50551176"
---
# <a name="overriding-a-dynamic-accessor"></a>Überschreiben einer dynamischen Zugriffsmethode

Bei Verwendung eine dynamische Zugriffsmethode wie z. B. `CDynamicAccessor`, den Befehl `Open` Methode erstellt einen Accessor, automatisch, basierend auf die Spalteninformationen des geöffneten Rowsets. Sie können die dynamischen Zugriffsmethode aus, um zu steuern, wie genau die Spalten gebunden sind, überschreiben.

Um die dynamischen Zugriffsmethode überschreiben möchten, übergeben **"false"** als letzten Parameter für die `CCommand::Open` Methode. Dies verhindert, dass `Open` aus einen Accessor automatisch erstellt. Sie können dann aufrufen `GetColumnInfo` , und rufen Sie `AddBindEntry` für jede Spalte, die Sie binden möchten. Der folgende Code zeigt, wie es geht:

```cpp
USES_CONVERSION;
double   dblProductID;

CCommand<CDynamicAccessor> product;
// Open the table, passing false to prevent automatic binding
product.Open(session, _T("Select * FROM Products"), NULL, NULL, DBGUID_DEFAULT, false);


ULONG         nColumns;
DBCOLUMNINFO*   pColumnInfo;
// Get the column information from the opened rowset.
product.GetColumnInfo(&nColumns, &pColumnInfo);

// Bind the product ID as a double.
pColumnInfo[0].wType          = DBTYPE_R8;
pColumnInfo[0].ulColumnSize = 8;
product.AddBindEntry(pColumnInfo[0]);

// Bind the product name as it is.
product.AddBindEntry(pColumnInfo[1]);

// Bind the reorder level as a string.
pColumnInfo[8].wType          = DBTYPE_STR;
pColumnInfo[8].ulColumnSize = 10;
product.AddBindEntry(pColumnInfo[8]);

// You have finished specifying the bindings. Go ahead and bind.
product.Bind();
// Free the memory for the column information that was retrieved in
// previous call to GetColumnInfo.
CoTaskMemFree(pColumnInfo);


char*   pszProductName;
char*   pszReorderLevel;
bool   bRC;

// Loop through the records tracing out the information.
while (product.MoveNext() == S_OK)
{
   bRC = product.GetValue(1, &dblProductID);
   pszProductName   = (char*)product.GetValue(2);
   pszReorderLevel  = (char*)product.GetValue(9);

   ATLTRACE(_T("Override = %lf \"%s\" \"%s\"\n"), dblProductID,
      A2T(pszProductName), A2T(pszReorderLevel));
}
```

## <a name="see-also"></a>Siehe auch

[Verwenden von Zugriffsmethoden](../../data/oledb/using-accessors.md)