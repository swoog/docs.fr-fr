---
title: Méthode SqlStreamChars.Seek (Int64, SeekOrigin) (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d52a1cd4dd70c29fc1af3fcf50c4f9b0c90125df
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827381"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a><span data-ttu-id="d7548-102">Méthode de SqlStreamChars.Seek (Int64, SeekOrigin)</span><span class="sxs-lookup"><span data-stu-id="d7548-102">SqlStreamChars.Seek(Int64, SeekOrigin) Method</span></span>

<span data-ttu-id="d7548-103">En cas de remplacement dans une classe dérivée, définit la position dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="d7548-103">When overridden in a derived class, sets the position within the current stream.</span></span> <span data-ttu-id="d7548-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="d7548-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="d7548-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7548-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="d7548-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="d7548-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a><span data-ttu-id="d7548-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7548-107">Parameters</span></span>

`offset`\
<span data-ttu-id="d7548-108">Offset d’octet par rapport à `origin`.</span><span class="sxs-lookup"><span data-stu-id="d7548-108">A byte offset relative to `origin`.</span></span>

`origin`\
<span data-ttu-id="d7548-109">Une des valeurs d’énumération qui indique le point de référence à partir de laquelle obtenir la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="d7548-109">One of the enumeration values that indicates the reference point from which to obtain the new position.</span></span>

## <a name="returns"></a><span data-ttu-id="d7548-110">Returns (Retours)</span><span class="sxs-lookup"><span data-stu-id="d7548-110">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="d7548-111">Nouvelle position dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="d7548-111">The new position within the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7548-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d7548-112">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="d7548-113">Le `SqlStreamChars.Seek` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="d7548-113">The `SqlStreamChars.Seek` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="d7548-114">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="d7548-114">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7548-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7548-115">Requirements</span></span>

<span data-ttu-id="d7548-116">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="d7548-116">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="d7548-117">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="d7548-117">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="d7548-118">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="d7548-118">**.NET Framework versions:** Available since 2.0.</span></span>