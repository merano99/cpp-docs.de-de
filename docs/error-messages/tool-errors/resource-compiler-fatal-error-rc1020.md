---
title: 'Ressourcencompiler: Schwerwiegender Fehler RC1020 | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: RC1020
dev_langs: C++
helpviewer_keywords: RC1020
ms.assetid: 3e073ebf-9136-4bf8-ac6a-3c642ed64594
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 2348e23183423a3d938a78ea691707428f6439b6
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="resource-compiler-fatal-error-rc1020"></a>Ressourcencompiler: Schwerwiegender Fehler RC1020
Unerwartetes "#endif"  
  
 Ein `#endif` Richtlinie angezeigt wurden, ohne ein passendes `#if`, **#ifdef**, oder **#ifndef** Richtlinie.  
  
 Stellen Sie sicher, dass es kein entsprechendes ist `#endif` für jede `#if`, **#ifdef**, und **#ifndef** Anweisung.