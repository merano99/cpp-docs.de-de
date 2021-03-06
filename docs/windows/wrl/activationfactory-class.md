---
title: ActivationFactory-Klasse
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::ActivationFactory
- module/Microsoft::WRL::ActivationFactory::ActivationFactory
- module/Microsoft::WRL::ActivationFactory::AddRef
- module/Microsoft::WRL::ActivationFactory::GetIids
- module/Microsoft::WRL::ActivationFactory::GetRuntimeClassName
- module/Microsoft::WRL::ActivationFactory::GetTrustLevel
- module/Microsoft::WRL::ActivationFactory::QueryInterface
- module/Microsoft::WRL::ActivationFactory::Release
helpviewer_keywords:
- Microsoft::WRL::ActivationFactory class
- Microsoft::WRL::ActivationFactory::ActivationFactory, constructor
- Microsoft::WRL::ActivationFactory::AddRef method
- Microsoft::WRL::ActivationFactory::GetIids method
- Microsoft::WRL::ActivationFactory::GetRuntimeClassName method
- Microsoft::WRL::ActivationFactory::GetTrustLevel method
- Microsoft::WRL::ActivationFactory::QueryInterface method
- Microsoft::WRL::ActivationFactory::Release method
ms.assetid: 5faddf1f-43b6-4f8a-97de-8c9d3ae1e1ff
ms.openlocfilehash: 8e5132f4a8711f6420cd9b52751550a96d10d8fc
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336006"
---
# <a name="activationfactory-class"></a>ActivationFactory-Klasse

Ermöglicht, dass eine oder mehrere Klassen durch die Windows-Runtime aktiviert werden.

## <a name="syntax"></a>Syntax

```cpp
template <
    typename I0 = Details::Nil,
    typename I1 = Details::Nil,
    typename I2 = Details::Nil
>
class ActivationFactory :
    public Details::RuntimeClass<
        typename Details::InterfaceListHelper<
            IActivationFactory,
            I0,
            I1,
            I2,
            Details::Nil
        >::TypeT,
        RuntimeClassFlags<WinRt | InhibitWeakReference>,
        false
    >;
```

### <a name="parameters"></a>Parameter

*I0*<br/>
Die nullte-Schnittstelle.

*I1*<br/>
Die erste Schnittstelle.

*I2*<br/>
Die zweite Schnittstelle.

## <a name="remarks"></a>Hinweise

`ActivationFactory` Stellt die Registrierungsmethoden und die grundlegenden Funktionen für die `IActivationFactory` Schnittstelle. `ActivationFactory` Außerdem können Sie eine benutzerdefinierte Factory-Implementierung bereitstellen.

Das folgende Codefragment veranschaulicht symbolisch ActivationFactory verwenden.

[!code-cpp[wrl-microsoft__wrl__activationfactory#1](../codesnippet/CPP/activationfactory-class_1.cpp)]

Das folgende Codefragment zeigt, wie Sie mit der [implementiert](implements-structure.md) Struktur an mehr als drei Schnittstellen-IDs.

`struct MyFactory : ActivationFactory<Implements<I1, I2, I3>, I4, I5>;`

## <a name="members"></a>Member

### <a name="public-constructors"></a>Öffentliche Konstruktoren

Name                                                       | Beschreibung
---------------------------------------------------------- | ------------------------------------------
[ActivationFactory::ActivationFactory](#activationfactory) | Initialisiert die `ActivationFactory` Klasse.

### <a name="public-methods"></a>Öffentliche Methoden

Name                                                           | Beschreibung
-------------------------------------------------------------- | --------------------------------------------------------------------------------------------
[ActivationFactory::AddRef](#addref)                           | Inkrementiert den Verweiszähler des aktuellen `ActivationFactory` Objekt.
[ActivationFactory::GetIids](#getiids)                         | Ruft ein Array von implementierten Schnittstellen-IDs ab.
[ActivationFactory::GetRuntimeClassName](#getruntimeclassname) | Ruft den Common Language Runtime-Klassennamen des Objekts ab, die die aktuelle `ActivationFactory` instanziiert.
[ActivationFactory::GetTrustLevel](#gettrustlevel)             | Ruft der Vertrauensebene des Objekts ab, das aktuelle `ActivationFactory` instanziiert.
[ActivationFactory::QueryInterface](#queryinterface)           | Ruft einen Zeiger auf die angegebene Schnittstelle ab.
[ActivationFactory::Release](#release)                         | Dekrementiert den Verweiszähler des aktuellen `ActivationFactory` Objekt.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

`I0`

`ChainInterfaces`

`I0`

`RuntimeClassBase`

`ImplementsHelper`

`DontUseNewUseMake`

`RuntimeClassFlags`

`RuntimeClassBaseT`

`RuntimeClass`

`ActivationFactory`

## <a name="requirements"></a>Anforderungen

**Header:** module.h

**Namespace:** Microsoft::WRL

## <a name="activationfactory"></a>ActivationFactory::ActivationFactory

Initialisiert die `ActivationFactory` Klasse.

```cpp
ActivationFactory();
```

## <a name="addref"></a>ActivationFactory::AddRef

Inkrementiert den Verweiszähler des aktuellen `ActivationFactory` Objekt.

```cpp
STDMETHOD_(
   ULONG,
   AddRef
)();
```

### <a name="return-value"></a>Rückgabewert

„S_OK“ im Erfolgsfall, andernfalls ein HRESULT, das den Fehler beschreibt.

## <a name="getiids"></a>ActivationFactory::GetIids

Ruft ein Array von implementierten Schnittstellen-IDs ab.

```cpp
STDMETHOD(
   GetIids
)(_Out_ ULONG *iidCount, _Deref_out_ _Deref_post_cap_(*iidCount) IID **iids);
```

### <a name="parameters"></a>Parameter

*iidCount*<br/>
Wenn dieser Vorgang abgeschlossen ist, die Anzahl der interace-IDs in die *Iids* Array.

*iids*<br/>
Wenn dieser Vorgang abgeschlossen ist, implementiert ein Array von Schnittstellen-IDs an.

### <a name="return-value"></a>Rückgabewert

„S_OK“ im Erfolgsfall, andernfalls ein HRESULT, das den Fehler beschreibt. E_OUTOFMEMORY ist möglicherweise ein Fehler HRESULT.

## <a name="getruntimeclassname"></a>ActivationFactory::GetRuntimeClassName

Ruft den Common Language Runtime-Klassennamen des Objekts ab, die die aktuelle `ActivationFactory` instanziiert.

```cpp
STDMETHOD(
   GetRuntimeClassName
)(_Out_ HSTRING* runtimeName);
```

### <a name="parameters"></a>Parameter

*runtimeName*<br/>
Wenn dieser Vorgang abgeschlossen ist, ein Handle für eine Zeichenfolge, die den Common Language Runtime-Klassennamen des Objekts enthält, die die aktuelle `ActivationFactory` instanziiert.

### <a name="return-value"></a>Rückgabewert

„S_OK“ im Erfolgsfall, andernfalls ein HRESULT, das den Fehler beschreibt.

## <a name="gettrustlevel"></a>ActivationFactory::GetTrustLevel

Ruft der Vertrauensebene des Objekts ab, das aktuelle `ActivationFactory` instanziiert.

```cpp
STDMETHOD(
   GetTrustLevel
)(_Out_ TrustLevel* trustLvl);
```

### <a name="parameters"></a>Parameter

*trustLvl*<br/>
Wenn dieser Vorgang abgeschlossen ist, die Vertrauensebene der Runtime-Klasse, die `ActivationFactory` instanziiert.

### <a name="return-value"></a>Rückgabewert

S_OK, wenn erfolgreich; Andernfalls wird ein Assertionsfehler ausgegeben und *TrustLvl* nastaven NA hodnotu `FullTrust`.

## <a name="queryinterface"></a>ActivationFactory::QueryInterface

Ruft einen Zeiger auf die angegebene Schnittstelle ab.

```cpp
STDMETHOD(
   QueryInterface
)(REFIID riid, _Deref_out_ void **ppvObject);
```

### <a name="parameters"></a>Parameter

*riid*<br/>
Eine Schnittstellen-ID.

*ppvObject*<br/>
Wenn dieser Vorgang abgeschlossen ist, ein Zeiger auf die Schnittstelle, die vom Parameter angegebene *Riid*.

### <a name="return-value"></a>Rückgabewert

„S_OK“ im Erfolgsfall, andernfalls ein HRESULT, das den Fehler beschreibt.

## <a name="release"></a>ActivationFactory::Release

Dekrementiert den Verweiszähler des aktuellen `ActivationFactory` Objekt.

```cpp
STDMETHOD_(
   ULONG,
   Release
)();
```

### <a name="return-value"></a>Rückgabewert

„S_OK“ im Erfolgsfall, andernfalls ein HRESULT, das den Fehler beschreibt.
