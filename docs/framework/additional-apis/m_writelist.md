---
title: Champ de Connection.m_WriteList
ms.date: 05/01/2017
topic_type:
- apiref
api_name:
- System.Net.Connection.m_WriteList
api_location:
- System.dll
api_type:
- Assembly
ms.assetid: 235503c1-1d01-4f59-895f-ae2cf15b3345
author: guardrex
ms.author: mairaw
ms.openlocfilehash: d145f6fd21989ada49a581ebf2694dcd56d94351
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32743158"
---
# <a name="connectionmwritelist-field"></a><span data-ttu-id="ce251-102">Connection.m\_WriteList champ</span><span class="sxs-lookup"><span data-stu-id="ce251-102">Connection.m\_WriteList Field</span></span>

<span data-ttu-id="ce251-103">`Connection.m_WriteList` est un <xref:System.Collections.ArrayList> de <xref:System.Net.HttpWebRequest> les objets qui sont la file d’attente d’être envoyés via HTTP.</span><span class="sxs-lookup"><span data-stu-id="ce251-103">`Connection.m_WriteList` is an <xref:System.Collections.ArrayList> of <xref:System.Net.HttpWebRequest> objects that are queued up to be sent over HTTP.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce251-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce251-104">Syntax</span></span>
  
```csharp  
private ArrayList m_WriteList
```

> [!WARNING]
> <span data-ttu-id="ce251-105">Le `Connection.m_WriteList` champ est privée et ne revient pas à être utilisée directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ce251-105">The `Connection.m_WriteList` field is private and not meant to be used directly in your code.</span></span>
> 
> <span data-ttu-id="ce251-106">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toutes circonstances.</span><span class="sxs-lookup"><span data-stu-id="ce251-106">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce251-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce251-107">Requirements</span></span>

<span data-ttu-id="ce251-108">**Namespace :** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="ce251-108">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="ce251-109">**Assembly :** système (dans System.dll)</span><span class="sxs-lookup"><span data-stu-id="ce251-109">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="ce251-110">**Versions du .NET framework :** disponible depuis la version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ce251-110">**.NET Framework versions:** Available since 2.0.</span></span>
