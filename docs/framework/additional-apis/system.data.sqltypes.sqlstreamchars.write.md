---
title: SqlStreamChars.Write (Char [], Int32, Int32), méthode (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: e8c8ee7ab7a744c1a1d18212f1c7f9788c91ea0d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152572"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a><span data-ttu-id="358ae-102">Méthode de SqlStreamChars.Write (Char [], Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="358ae-102">SqlStreamChars.Write(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="358ae-103">En cas de substitution dans une classe dérivée, écrit une séquence de caractères dans le flux actuel et avance la position actuelle dans ce flux du nombre de caractères écrits.</span><span class="sxs-lookup"><span data-stu-id="358ae-103">When overridden in a derived class, writes a sequence of characters to the current stream and advances the current position within this stream by the number of characters written.</span></span> <span data-ttu-id="358ae-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="358ae-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="358ae-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="358ae-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="358ae-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="358ae-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="358ae-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="358ae-107">Parameters</span></span>

`buffer`  
<span data-ttu-id="358ae-108">Un tableau de caractères à écrire.</span><span class="sxs-lookup"><span data-stu-id="358ae-108">A char array to write.</span></span>

`offset`  
<span data-ttu-id="358ae-109">Un décalage relatif à l’origine.</span><span class="sxs-lookup"><span data-stu-id="358ae-109">An offset relative to origin.</span></span>

`count`  
<span data-ttu-id="358ae-110">Le nombre de caractères à écrire dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="358ae-110">The number of characters to be written to the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="358ae-111">Notes</span><span class="sxs-lookup"><span data-stu-id="358ae-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="358ae-112">Le `SqlStreamChars.Write` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="358ae-112">The `SqlStreamChars.Write` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="358ae-113">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="358ae-113">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="358ae-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="358ae-114">Requirements</span></span>

<span data-ttu-id="358ae-115">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="358ae-115">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="358ae-116">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="358ae-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="358ae-117">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="358ae-117">**.NET Framework versions:** Available since 2.0.</span></span>