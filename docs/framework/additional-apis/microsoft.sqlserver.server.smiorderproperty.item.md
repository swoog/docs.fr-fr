---
title: Propriété SmiOrderProperty.Item (Microsoft.SqlServer.Server)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- Microsoft.SqlServer.Server.SmiOrderProperty.Item
- Microsoft.SqlServer.Server.SmiOrderProperty.get_Item
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: cb2f6cb956f9571f9bd2ba7f86d79c5df6e72a15
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827732"
---
# <a name="smiorderpropertyitem-property"></a><span data-ttu-id="a2bf2-102">Propriété de SmiOrderProperty.Item</span><span class="sxs-lookup"><span data-stu-id="a2bf2-102">SmiOrderProperty.Item Property</span></span>

<span data-ttu-id="a2bf2-103">Obtient l’ordre des colonnes pour l’entité.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-103">Gets the column order for the entity.</span></span> <span data-ttu-id="a2bf2-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="a2bf2-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="a2bf2-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bf2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2bf2-107">Syntax</span></span>

```csharp
internal SmiColumnOrder Item { get; }
```

## <a name="property-value"></a><span data-ttu-id="a2bf2-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="a2bf2-108">Property value</span></span>

<span data-ttu-id="a2bf2-109">L’ordre des colonnes.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-109">The column order.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2bf2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a2bf2-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="a2bf2-111">Le `SmiOrderProperty.Item` propriété est interne et n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-111">The `SmiOrderProperty.Item` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="a2bf2-112">Microsoft ne prend pas en charge l’utilisation de cette propriété dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-112">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2bf2-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a2bf2-113">Requirements</span></span>

<span data-ttu-id="a2bf2-114">**Espace de noms :** <xref:Microsoft.SqlServer.Server></span><span class="sxs-lookup"><span data-stu-id="a2bf2-114">**Namespace:** <xref:Microsoft.SqlServer.Server></span></span>

<span data-ttu-id="a2bf2-115">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="a2bf2-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="a2bf2-116">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="a2bf2-116">**.NET Framework versions:** Available since 2.0.</span></span>