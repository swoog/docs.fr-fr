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
ms.openlocfilehash: c9162e123c1167e3aa1be26ddd37279c088acc89
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149161"
---
# <a name="connectiongroupmconnectionlist-field"></a>ConnectionGroup.m\_ConnectionList champ

`ConnectionGroup.m_ConnectionList` est un <xref:System.Collections.ArrayList> des objets de connexion qui sert le même URI et le partage les mêmes valeurs pour d’autres propriétés comme expiration et l’authentification.

## <a name="syntax"></a>Syntaxe
  
```csharp  
private ArrayList m_ConnectionList
```

> [!WARNING]
> Le `ConnectionGroup.m_ConnectionList` champ est privé et n’est pas destiné à être utilisé directement dans votre code.
> 
> Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.

## <a name="requirements"></a>Spécifications

**Espace de noms :** <xref:System.Net>

**Assembly :** Système (dans System.dll)

**Versions du .NET framework :** Disponible à partir de 2.0.
