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
ms.openlocfilehash: a7446b9cbbfd4d3a4d38368a8e24c99527cf9108
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705933"
---
# <a name="connectionmwritelist-field"></a><span data-ttu-id="ffb06-102">Connection.m\_WriteList champ</span><span class="sxs-lookup"><span data-stu-id="ffb06-102">Connection.m\_WriteList Field</span></span>

<span data-ttu-id="ffb06-103">`Connection.m_WriteList` est un <xref:System.Collections.ArrayList> de <xref:System.Net.HttpWebRequest> les objets qui sont la file d’attente d’être envoyés via HTTP.</span><span class="sxs-lookup"><span data-stu-id="ffb06-103">`Connection.m_WriteList` is an <xref:System.Collections.ArrayList> of <xref:System.Net.HttpWebRequest> objects that are queued up to be sent over HTTP.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb06-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffb06-104">Syntax</span></span>
  
```csharp  
private ArrayList m_WriteList
```

> [!WARNING]
> <span data-ttu-id="ffb06-105">Le `Connection.m_WriteList` champ est privé et n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ffb06-105">The `Connection.m_WriteList` field is private and is not meant to be used directly in your code.</span></span>
> 
> <span data-ttu-id="ffb06-106">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="ffb06-106">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb06-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffb06-107">Requirements</span></span>

<span data-ttu-id="ffb06-108">**Espace de noms :** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="ffb06-108">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="ffb06-109">**Assembly :** Système (dans System.dll)</span><span class="sxs-lookup"><span data-stu-id="ffb06-109">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="ffb06-110">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="ffb06-110">**.NET Framework versions:** Available since 2.0.</span></span>
