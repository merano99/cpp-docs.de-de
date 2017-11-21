---
title: '&lt;fstream&gt; typedefs | Microsoft-Dokumentation'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- fstream/std::filebuf
- fstream/std::fstream
- fstream/std::ifstream
- fstream/std::ofstream
- fstream/std::wfilebuf
- fstream/std::wfstream
- fstream/std::wifstream
- fstream/std::wofstream
ms.assetid: 8dddef2d-7f17-42a6-ba08-6f6f20597d23
caps.latest.revision: "11"
manager: ghogen
ms.openlocfilehash: 55a148c472048c5531521cd6f4574477e7c31cac
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="ltfstreamgt-typedefs"></a>&lt;fstream&gt; typedefs (<fstream>-Typdefinitionen)
||||  
|-|-|-|  
|[filebuf](#filebuf)|[fstream](#fstream)|[ifstream](#ifstream)|  
|[ofstream](#ofstream)|[wfilebuf](#wfilebuf)|[wfstream](#wfstream)|  
|[wifstream](#wifstream)|[wofstream](#wofstream)|  
  
##  <a name="filebuf"></a> filebuf  
 Ein `basic_filebuf`-Typ, der auf `char`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_filebuf<char, char_traits<char>> filebuf;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_filebuf](../standard-library/basic-filebuf-class.md), die auf Elemente vom Typ `char` mit Standardzeichenmerkmalen spezialisiert ist.  
  
##  <a name="fstream"></a> fstream  
 Ein `basic_fstream`-Typ, der auf `char`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_fstream<char, char_traits<char>> fstream;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_fstream](../standard-library/basic-fstream-class.md), die für Elemente des Typs `char` mit Standardzeichenmerkmalen spezialisiert ist.  
  
##  <a name="ifstream"></a> ifstream  
 Definiert einen Stream, der für das serielle Lesen von Einzelbyte-Zeichendaten aus einer Datei verwendet werden soll. `ifstream` ist eine typedef, die die Vorlagenklasse `basic_ifstream` für `char` spezialisiert.  
  
 Es gibt auch `wifstream`, eine typedef, die `basic_ifstream` zum Lesen von doppelt breiten `wchar_t`-Zeichen spezialisiert. Weitere Informationen finden Sie unter [wifstream](../standard-library/fstream-typedefs.md#wifstream).  
  
```
typedef basic_ifstream<char, char_traits<char>> ifstream;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse `basic_ifstream`, die auf Elemente vom Typ "char" mit Standard-Zeichenmerkmale spezialisiert ist. Ein Beispiel ist  
  
 `using namespace std;`  
  
 `ifstream infile("existingtextfile.txt");`  
  
 `if (!infile.bad())`  
  
 `{`  
  
 `// Dump the contents of the file to cout.`  
  
 `cout << infile.rdbuf();`  
  
 `infile.close();`  
  
 `}`  
  
##  <a name="ofstream"></a> ofstream  
 Ein `basic_ofstream`-Typ, der auf `char`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_ofstream<char, char_traits<char>> ofstream;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_ofstream](../standard-library/basic-ofstream-class.md), die auf Elemente vom Typ `char` mit Standardzeichenmerkmalen spezialisiert ist.  
  
##  <a name="wfstream"></a> wfstream  
 Ein `basic_fstream`-Typ, der auf `wchar_t`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_fstream<wchar_t, char_traits<wchar_t>> wfstream;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_fstream](../standard-library/basic-fstream-class.md), die für Elemente des Typs `wchar_t` mit Standardzeichenmerkmalen spezialisiert ist.  
  
##  <a name="wifstream"></a> wifstream  
 Ein `basic_ifstream`-Typ, der auf `wchar_t`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_ifstream<wchar_t, char_traits<wchar_t>> wifstream;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_ifstream](../standard-library/basic-ifstream-class.md), die auf Elemente des Typs `wchar_t` mit Standardzeichenmerkmalen spezialisiert ist.  
  
##  <a name="wofstream"></a> wofstream  
 Ein `basic_ofstream`-Typ, der auf `wchar_t`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_ofstream<wchar_t, char_traits<wchar_t>> wofstream;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_ofstream](../standard-library/basic-ofstream-class.md), die auf Elemente vom Typ `wchar_t` mit Standardzeichenmerkmalen spezialisiert ist.  
  
##  <a name="wfilebuf"></a> wfilebuf  
 Ein `basic_filebuf`-Typ, der auf `wchar_t`-Vorlagenparameter spezialisiert ist.  
  
```
typedef basic_filebuf<wchar_t, char_traits<wchar_t>> wfilebuf;
```  
  
### <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für die Vorlagenklasse [basic_filebuf](../standard-library/basic-filebuf-class.md), die auf Elemente vom Typ `wchar_t` mit Standardzeichenmerkmalen spezialisiert ist.  
  
## <a name="see-also"></a>Siehe auch  
 [\<fstream>](../standard-library/fstream.md)


