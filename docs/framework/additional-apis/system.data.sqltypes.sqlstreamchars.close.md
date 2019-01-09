---
title: Méthode SqlStreamChars.Close (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Close
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 893ee729b864d381c4e4686024687f309d15d214
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152652"
---
# <a name="sqlstreamcharsclose-method"></a><span data-ttu-id="cfcbc-102">SqlStreamChars.Close (méthode)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-102">SqlStreamChars.Close Method</span></span>

<span data-ttu-id="cfcbc-103">Ferme le flux actuel et libère toutes les ressources système associées au flux.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-103">Closes the current stream and releases any system resources associated with the stream.</span></span> <span data-ttu-id="cfcbc-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="cfcbc-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-105">It's intended for use by SQL Server.</span></span><span data-ttu-id="cfcbc-106"> Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-106"> For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public virtual void Close ();
```

## <a name="remarks"></a><span data-ttu-id="cfcbc-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cfcbc-107">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="cfcbc-108">Le `SqlStreamChars.Close` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-108">The `SqlStreamChars.Close` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="cfcbc-109">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-109">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfcbc-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cfcbc-110">Requirements</span></span>

<span data-ttu-id="cfcbc-111">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="cfcbc-111">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="cfcbc-112">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-112">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="cfcbc-113">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-113">**.NET Framework versions:** Available since 2.0.</span></span>