---
title: Champ de ConnectionGroup.m_ConnectionList
ms.date: 05/01/2017
topic_type:
- apiref
api_name:
- System.Net.ConnectionGroup.m_ConnectionList
api_location:
- System.dll
api_type:
- Assembly
ms.assetid: 186083cf-8dff-4600-a2ab-6fed4b4de6af
author: guardrex
ms.author: mairaw
ms.openlocfilehash: 5844f8d63aa5646bfd7860dc0407528fb2eaf329
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="connectiongroupmconnectionlist-field"></a>ConnectionGroup.m\_ConnectionList champ

`ConnectionGroup.m_ConnectionList` est un <xref:System.Collections.ArrayList> des objets de connexion qui a le même URI et le partage les mêmes valeurs pour d’autres propriétés comme expiration et l’authentification.

## <a name="syntax"></a>Syntaxe
  
```csharp  
private ArrayList m_ConnectionList
```

> [!WARNING]
> Le `ConnectionGroup.m_ConnectionList` champ est privée et ne revient pas à être utilisée directement dans votre code.
> 
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toutes circonstances.

## <a name="requirements"></a>Spécifications

**Namespace :** <xref:System.Net>

**Assembly :** système (dans System.dll)

**Versions du .NET framework :** disponible depuis la version 2.0.
