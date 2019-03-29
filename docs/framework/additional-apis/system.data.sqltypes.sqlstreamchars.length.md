---
title: Propriété SqlStreamChars.Length (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Length
- System.Data.SqlTypes.SqlStreamChars.get_Length
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: c2ef66fa493512e1fa062e22858ea251ced39453
ms.sourcegitcommit: d938c39afb9216db377d0f0ecdaa53936a851059
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58634139"
---
# <a name="sqlstreamcharslength-property"></a><span data-ttu-id="a5264-102">Propriété de SqlStreamChars.Length</span><span class="sxs-lookup"><span data-stu-id="a5264-102">SqlStreamChars.Length Property</span></span>

<span data-ttu-id="a5264-103">En cas de substitution dans une classe dérivée, obtient la longueur du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="a5264-103">When overridden in a derived class, gets the length of the current stream.</span></span> <span data-ttu-id="a5264-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="a5264-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="a5264-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5264-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="a5264-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="a5264-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5264-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5264-107">Syntax</span></span>

```csharp
public abstract long Length { get; }
```

## <a name="property-value"></a><span data-ttu-id="a5264-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="a5264-108">Property value</span></span>

<xref:System.Int64>\
<span data-ttu-id="a5264-109">Longueur du flux.</span><span class="sxs-lookup"><span data-stu-id="a5264-109">The length of the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5264-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a5264-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="a5264-111">Le `SqlStreamChars.Length` propriété est privée et qu’il n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a5264-111">The `SqlStreamChars.Length` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="a5264-112">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="a5264-112">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5264-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5264-113">Requirements</span></span>

<span data-ttu-id="a5264-114">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="a5264-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="a5264-115">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="a5264-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="a5264-116">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="a5264-116">**.NET Framework versions:** Available since 2.0.</span></span>