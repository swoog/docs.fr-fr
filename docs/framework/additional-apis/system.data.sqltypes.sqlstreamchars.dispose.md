---
title: Méthode SqlStreamChars.Dispose(Boolean) (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Dispose
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 930a4a69c6c44269e728fbcef62e561ab165ea22
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222361"
---
# <a name="sqlstreamcharsdisposeboolean-method"></a><span data-ttu-id="bfd04-102">SqlStreamChars.Dispose(Boolean) (méthode)</span><span class="sxs-lookup"><span data-stu-id="bfd04-102">SqlStreamChars.Dispose(Boolean) Method</span></span>

<span data-ttu-id="bfd04-103">En cas de substitution dans une classe dérivée, libère les ressources utilisées par le flux.</span><span class="sxs-lookup"><span data-stu-id="bfd04-103">When overridden in a derived class, releases the resources used by the stream.</span></span> <span data-ttu-id="bfd04-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="bfd04-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="bfd04-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bfd04-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="bfd04-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="bfd04-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
protected virtual void Dispose (bool disposing);
```

## <a name="parameters"></a><span data-ttu-id="bfd04-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfd04-107">Parameters</span></span>

`disposing`\
<span data-ttu-id="bfd04-108">`true` pour libérer les ressources managées et non managées ; `false` pour ne libérer que les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="bfd04-108">`true` to release both managed and unmanaged resources; `false` to release only unmanaged resources.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfd04-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bfd04-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="bfd04-110">Le `SqlStreamChars.Dispose` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="bfd04-110">The `SqlStreamChars.Dispose` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="bfd04-111">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="bfd04-111">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd04-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bfd04-112">Requirements</span></span>

<span data-ttu-id="bfd04-113">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="bfd04-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="bfd04-114">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="bfd04-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="bfd04-115">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="bfd04-115">**.NET Framework versions:** Available since 2.0.</span></span>