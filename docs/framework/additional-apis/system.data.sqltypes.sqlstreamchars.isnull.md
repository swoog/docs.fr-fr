---
title: Propriété SqlStreamChars.IsNull (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.IsNull
- System.Data.SqlTypes.SqlStreamChars.get_IsNull
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 79ebb9ec54185a94cb95dfd0fb2929e61cf513ef
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152622"
---
# <a name="sqlstreamcharsisnull-property"></a><span data-ttu-id="a577a-102">Propriété de SqlStreamChars.IsNull</span><span class="sxs-lookup"><span data-stu-id="a577a-102">SqlStreamChars.IsNull Property</span></span>

<span data-ttu-id="a577a-103">En cas de substitution dans une classe dérivée, obtient une valeur qui indique si le flux est `null`.</span><span class="sxs-lookup"><span data-stu-id="a577a-103">When overridden in a derived class, gets a value that indicates whether the stream is `null`.</span></span> <span data-ttu-id="a577a-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="a577a-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="a577a-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a577a-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="a577a-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="a577a-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a577a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a577a-107">Syntax</span></span>

```csharp
public abstract bool IsNull { get; }
```

## <a name="property-value"></a><span data-ttu-id="a577a-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="a577a-108">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="a577a-109">`true` Si le flux est `null`; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="a577a-109">`true` if the stream is `null`; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a577a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a577a-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="a577a-111">Le `SqlStreamChars.IsNull` propriété est privée et qu’il n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a577a-111">The `SqlStreamChars.IsNull` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="a577a-112">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="a577a-112">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="a577a-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a577a-113">Requirements</span></span>

<span data-ttu-id="a577a-114">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="a577a-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="a577a-115">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="a577a-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="a577a-116">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="a577a-116">**.NET Framework versions:** Available since 2.0.</span></span>