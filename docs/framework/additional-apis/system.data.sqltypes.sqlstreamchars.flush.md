---
title: Méthode SqlStreamChars.Flush (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Flush
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: ecaf7932a4e832a88b883ceac4746afe6140b38e
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152742"
---
# <a name="sqlstreamcharsflush-method"></a><span data-ttu-id="9b7be-102">SqlStreamChars.Flush (méthode)</span><span class="sxs-lookup"><span data-stu-id="9b7be-102">SqlStreamChars.Flush Method</span></span>

<span data-ttu-id="9b7be-103">En cas de remplacement dans une classe dérivée, efface toutes les mémoires tampons pour ce flux et provoque l'écriture de toutes les données se trouvant dans des mémoires tampons sur l'appareil sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9b7be-103">When overridden in a derived class, clears all buffers for this stream and causes any buffered data to be written to the underlying device.</span></span> <span data-ttu-id="9b7be-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="9b7be-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="9b7be-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9b7be-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="9b7be-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="9b7be-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b7be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b7be-107">Syntax</span></span>

```csharp
public abstract void Flush ();
```

## <a name="remarks"></a><span data-ttu-id="9b7be-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9b7be-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="9b7be-109">Le `SqlStreamChars.Flush` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="9b7be-109">The `SqlStreamChars.Flush` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="9b7be-110">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="9b7be-110">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b7be-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b7be-111">Requirements</span></span>

<span data-ttu-id="9b7be-112">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="9b7be-112">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="9b7be-113">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="9b7be-113">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="9b7be-114">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="9b7be-114">**.NET Framework versions:** Available since 2.0.</span></span>