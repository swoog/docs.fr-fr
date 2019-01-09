---
title: Propriété SqlChars.Stream (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlChars.Stream
- System.Data.SqlTypes.SqlChars.get_Stream
- System.Data.SqlTypes.SqlChars.set_Stream
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: f8b6f4f3a92f1d78e434263c6a7897641867c412
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152602"
---
# <a name="sqlcharsstream-property"></a><span data-ttu-id="ae8a7-102">Propriété de SqlChars.Stream</span><span class="sxs-lookup"><span data-stu-id="ae8a7-102">SqlChars.Stream Property</span></span>

<span data-ttu-id="ae8a7-103">Obtient ou définit le flux de caractères.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-103">Gets or sets the character stream.</span></span> <span data-ttu-id="ae8a7-104">L’assembly qui contient cette propriété a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="ae8a7-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="ae8a7-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
internal SqlStreamChars Stream { get; set; }
```

## <a name="property-value"></a><span data-ttu-id="ae8a7-107">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="ae8a7-107">Property value</span></span>

`System.Data.SqlTypes.SqlStreamChars`\
<span data-ttu-id="ae8a7-108">Le flux de caractères.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-108">The character stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae8a7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ae8a7-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="ae8a7-110">Le `SqlChars.Stream` propriété est interne et n’est pas destinée à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-110">The `SqlChars.Stream` property is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="ae8a7-111">Microsoft ne prend pas en charge l’utilisation de cette propriété dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-111">Microsoft does not support the use of this property in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8a7-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae8a7-112">Requirements</span></span>

<span data-ttu-id="ae8a7-113">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="ae8a7-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="ae8a7-114">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="ae8a7-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="ae8a7-115">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-115">**.NET Framework versions:** Available since 2.0.</span></span>