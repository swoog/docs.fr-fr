---
title: Propriété SqlStreamChars.IsNull (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.IsNull
- System.Data.SqlTypes.SqlStreamChars.get_IsNull
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 03b702b0ffe258eb8cad0a1ece5314b363f9a0d0
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65634613"
---
# <a name="sqlstreamcharsisnull-property"></a><span data-ttu-id="a3b65-102">Propriété de SqlStreamChars.IsNull</span><span class="sxs-lookup"><span data-stu-id="a3b65-102">SqlStreamChars.IsNull Property</span></span>

<span data-ttu-id="a3b65-103">En cas de substitution dans une classe dérivée, obtient une valeur qui indique si le flux est `null`.</span><span class="sxs-lookup"><span data-stu-id="a3b65-103">When overridden in a derived class, gets a value that indicates whether the stream is `null`.</span></span> <span data-ttu-id="a3b65-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="a3b65-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="a3b65-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a3b65-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="a3b65-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="a3b65-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b65-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3b65-107">Syntax</span></span>

```csharp
public abstract bool IsNull { get; }
```

## <a name="property-value"></a><span data-ttu-id="a3b65-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="a3b65-108">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="a3b65-109">`true` Si le flux est `null`; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="a3b65-109">`true` if the stream is `null`; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3b65-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a3b65-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="a3b65-111">Le `SqlStreamChars.IsNull` propriété est privée et qu’il n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a3b65-111">The `SqlStreamChars.IsNull` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="a3b65-112">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="a3b65-112">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b65-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3b65-113">Requirements</span></span>

<span data-ttu-id="a3b65-114">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="a3b65-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="a3b65-115">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="a3b65-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="a3b65-116">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="a3b65-116">**.NET Framework versions:** Available since 2.0.</span></span>
