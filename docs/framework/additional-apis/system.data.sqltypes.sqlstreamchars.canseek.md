---
title: Propriété SqlStreamChars.CanSeek (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/19/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.CanSeek
- System.Data.SqlTypes.SqlStreamChars.get_CanSeek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 52f88a3551e20c74d7a1144c3cd6859a023980db
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675173"
---
# <a name="sqlstreamcharscanseek-property"></a><span data-ttu-id="61079-102">Propriété de SqlStreamChars.CanSeek</span><span class="sxs-lookup"><span data-stu-id="61079-102">SqlStreamChars.CanSeek Property</span></span>

<span data-ttu-id="61079-103">En cas de substitution dans une classe dérivée, obtient une valeur qui indique si le flux actuel prend en charge l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="61079-103">When overridden in a derived class, gets a value that indicates whether the current steam supports the seek operation.</span></span> <span data-ttu-id="61079-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="61079-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="61079-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61079-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="61079-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="61079-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract bool CanSeek { get; }
```

## <a name="property-value"></a><span data-ttu-id="61079-107">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="61079-107">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="61079-108">`true` Si le flux actuel prend en charge l’opération de recherche ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="61079-108">`true` if the current steam supports the seek operation; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="61079-109">Notes</span><span class="sxs-lookup"><span data-stu-id="61079-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="61079-110">Le `SqlStreamChars.CanSeek` propriété est privée et qu’il n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="61079-110">The `SqlStreamChars.CanSeek` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="61079-111">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="61079-111">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="61079-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61079-112">Requirements</span></span>

<span data-ttu-id="61079-113">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="61079-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="61079-114">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="61079-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="61079-115">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="61079-115">**.NET Framework versions:** Available since 2.0.</span></span>