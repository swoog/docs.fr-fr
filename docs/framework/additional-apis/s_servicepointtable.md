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
ms.openlocfilehash: 5450a0cb3e5bd39a86365b16d372c7e573a43496
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33351756"
---
# <a name="servicepointmanagersservicepointtable-field"></a><span data-ttu-id="f859e-102">ServicePointManager.s\_ServicePointTable champ</span><span class="sxs-lookup"><span data-stu-id="f859e-102">ServicePointManager.s\_ServicePointTable Field</span></span>

<span data-ttu-id="f859e-103">`ServicePointManager.s_ServicePointTable` est un <xref:System.Collections.Hashtable> qui contient la liste des connexions HTTP actives (<xref:System.Net.ServicePoint>s) dans le <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="f859e-103">`ServicePointManager.s_ServicePointTable` is a <xref:System.Collections.Hashtable> that contains the list of active HTTP connections (<xref:System.Net.ServicePoint>s) in the <xref:System.AppDomain>.</span></span>

## <a name="syntax"></a><span data-ttu-id="f859e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f859e-104">Syntax</span></span>
  
```csharp  
private static Hashtable s_ServicePointTable
```

> [!WARNING]
> <span data-ttu-id="f859e-105">Le `ServicePointManager.s_ServicePointTable` champ est privée et ne revient pas à être utilisée directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="f859e-105">The `ServicePointManager.s_ServicePointTable` field is private and not meant to be used directly in your code.</span></span>
> 
> <span data-ttu-id="f859e-106">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toutes circonstances.</span><span class="sxs-lookup"><span data-stu-id="f859e-106">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="f859e-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f859e-107">Requirements</span></span>

<span data-ttu-id="f859e-108">**Namespace :** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="f859e-108">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="f859e-109">**Assembly :** système (dans System.dll)</span><span class="sxs-lookup"><span data-stu-id="f859e-109">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="f859e-110">**Versions du .NET framework :** disponible depuis la version 2.0.</span><span class="sxs-lookup"><span data-stu-id="f859e-110">**.NET Framework versions:** Available since 2.0.</span></span>
