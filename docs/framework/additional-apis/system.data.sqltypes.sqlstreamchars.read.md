---
title: SqlStreamChars.Read (Char [], Int32, Int32), méthode (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Read
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 87bff6dd78743ae08a5a3db8a783b56a0b7c3f24
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152532"
---
# <a name="sqlstreamcharsreadchar-int32-int32-method"></a><span data-ttu-id="d8fe6-102">Méthode de SqlStreamChars.Read (Char [], Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="d8fe6-102">SqlStreamChars.Read(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="d8fe6-103">En cas de substitution dans une classe dérivée, lit le jeu de caractères suivant dans le flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-103">When overridden in a derived class, reads the next set of characters from the input stream.</span></span> <span data-ttu-id="d8fe6-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="d8fe6-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="d8fe6-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract int Read (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="d8fe6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8fe6-107">Parameters</span></span>

`buffer`\
<span data-ttu-id="d8fe6-108">Un tableau de caractères à lire.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-108">A char array to read.</span></span>

`offset`\
<span data-ttu-id="d8fe6-109">Un décalage relatif à l’origine.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-109">An offset relative to origin.</span></span>

`count`\
<span data-ttu-id="d8fe6-110">Le nombre de caractères à lire à partir du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-110">The number of characters to be read from the current stream.</span></span>

## <a name="returns"></a><span data-ttu-id="d8fe6-111">Returns (Retours)</span><span class="sxs-lookup"><span data-stu-id="d8fe6-111">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="d8fe6-112">Nombre total de caractères lus dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-112">The total number of characters read into the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fe6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d8fe6-113">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="d8fe6-114">Le `SqlStreamChars.Read` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-114">The `SqlStreamChars.Read` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="d8fe6-115">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-115">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8fe6-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8fe6-116">Requirements</span></span>

<span data-ttu-id="d8fe6-117">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="d8fe6-117">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="d8fe6-118">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="d8fe6-118">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="d8fe6-119">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="d8fe6-119">**.NET Framework versions:** Available since 2.0.</span></span>