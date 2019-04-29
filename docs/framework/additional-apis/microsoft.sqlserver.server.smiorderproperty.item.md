---
title: Propriété SmiOrderProperty.Item (Microsoft.SqlServer.Server)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- Microsoft.SqlServer.Server.SmiOrderProperty.Item
- Microsoft.SqlServer.Server.SmiOrderProperty.get_Item
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 499522a11cac744c14ac32cf3bfe485a46b19d93
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675310"
---
# <a name="smiorderpropertyitem-property"></a><span data-ttu-id="f9e4b-102">Propriété de SmiOrderProperty.Item</span><span class="sxs-lookup"><span data-stu-id="f9e4b-102">SmiOrderProperty.Item Property</span></span>

<span data-ttu-id="f9e4b-103">Obtient l’ordre des colonnes pour l’entité.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-103">Gets the column order for the entity.</span></span> <span data-ttu-id="f9e4b-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="f9e4b-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="f9e4b-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e4b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9e4b-107">Syntax</span></span>

```csharp
internal SmiColumnOrder Item { get; }
```

## <a name="property-value"></a><span data-ttu-id="f9e4b-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="f9e4b-108">Property value</span></span>

<span data-ttu-id="f9e4b-109">L’ordre des colonnes.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-109">The column order.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e4b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f9e4b-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="f9e4b-111">Le `SmiOrderProperty.Item` propriété est interne et n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-111">The `SmiOrderProperty.Item` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="f9e4b-112">Microsoft ne prend pas en charge l’utilisation de cette propriété dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-112">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e4b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9e4b-113">Requirements</span></span>

<span data-ttu-id="f9e4b-114">**Espace de noms :** <xref:Microsoft.SqlServer.Server></span><span class="sxs-lookup"><span data-stu-id="f9e4b-114">**Namespace:** <xref:Microsoft.SqlServer.Server></span></span>

<span data-ttu-id="f9e4b-115">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="f9e4b-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="f9e4b-116">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-116">**.NET Framework versions:** Available since 2.0.</span></span>