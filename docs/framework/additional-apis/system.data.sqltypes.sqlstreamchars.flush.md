---
title: Méthode SqlStreamChars.Flush (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Flush
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 8cd24a5ca420552f283da61ecd4edcad02965403
ms.sourcegitcommit: d938c39afb9216db377d0f0ecdaa53936a851059
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58634191"
---
# <a name="sqlstreamcharsflush-method"></a><span data-ttu-id="3ca8b-102">SqlStreamChars.Flush (méthode)</span><span class="sxs-lookup"><span data-stu-id="3ca8b-102">SqlStreamChars.Flush Method</span></span>

<span data-ttu-id="3ca8b-103">En cas de remplacement dans une classe dérivée, efface toutes les mémoires tampons pour ce flux et provoque l'écriture de toutes les données se trouvant dans des mémoires tampons sur l'appareil sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-103">When overridden in a derived class, clears all buffers for this stream and causes any buffered data to be written to the underlying device.</span></span> <span data-ttu-id="3ca8b-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="3ca8b-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="3ca8b-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca8b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ca8b-107">Syntax</span></span>

```csharp
public abstract void Flush ();
```

## <a name="remarks"></a><span data-ttu-id="3ca8b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3ca8b-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="3ca8b-109">Le `SqlStreamChars.Flush` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-109">The `SqlStreamChars.Flush` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="3ca8b-110">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-110">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca8b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ca8b-111">Requirements</span></span>

<span data-ttu-id="3ca8b-112">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="3ca8b-112">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="3ca8b-113">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="3ca8b-113">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="3ca8b-114">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="3ca8b-114">**.NET Framework versions:** Available since 2.0.</span></span>