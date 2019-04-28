---
title: Champ de ServicePointManager.s_ServicePointTable
ms.date: 05/01/2017
topic_type:
- apiref
api_name:
- System.Net.ServicePointManager.s_ServicePointTable
api_location:
- System.dll
api_type:
- Assembly
ms.assetid: 24459679-291c-401a-9def-e42b29466fcf
author: guardrex
ms.author: mairaw
ms.openlocfilehash: ebcf5c3f13b3bd30a8e091be09ae546eee1eaffe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675440"
---
# <a name="servicepointmanagersservicepointtable-field"></a><span data-ttu-id="c0a3f-102">ServicePointManager.s\_ServicePointTable champ</span><span class="sxs-lookup"><span data-stu-id="c0a3f-102">ServicePointManager.s\_ServicePointTable Field</span></span>

<span data-ttu-id="c0a3f-103">`ServicePointManager.s_ServicePointTable` est un <xref:System.Collections.Hashtable> qui contient la liste des connexions HTTP actives (<xref:System.Net.ServicePoint>s) dans le <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-103">`ServicePointManager.s_ServicePointTable` is a <xref:System.Collections.Hashtable> that contains the list of active HTTP connections (<xref:System.Net.ServicePoint>s) in the <xref:System.AppDomain>.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a3f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0a3f-104">Syntax</span></span>
  
```csharp  
private static Hashtable s_ServicePointTable
```

> [!WARNING]
> <span data-ttu-id="c0a3f-105">Le `ServicePointManager.s_ServicePointTable` champ est privé et n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-105">The `ServicePointManager.s_ServicePointTable` field is private and is not meant to be used directly in your code.</span></span>
> 
> <span data-ttu-id="c0a3f-106">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-106">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a3f-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0a3f-107">Requirements</span></span>

<span data-ttu-id="c0a3f-108">**Espace de noms :** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="c0a3f-108">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="c0a3f-109">**Assembly :** Système (dans System.dll)</span><span class="sxs-lookup"><span data-stu-id="c0a3f-109">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="c0a3f-110">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="c0a3f-110">**.NET Framework versions:** Available since 2.0.</span></span>
