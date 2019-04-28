---
title: SqlStreamChars.Write (Char [], Int32, Int32), méthode (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 4084c7161eaa91d78eab32f1c14624e0032cdfcf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705907"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a><span data-ttu-id="cd944-102">Méthode de SqlStreamChars.Write (Char [], Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="cd944-102">SqlStreamChars.Write(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="cd944-103">En cas de substitution dans une classe dérivée, écrit une séquence de caractères dans le flux actuel et avance la position actuelle dans ce flux du nombre de caractères écrits.</span><span class="sxs-lookup"><span data-stu-id="cd944-103">When overridden in a derived class, writes a sequence of characters to the current stream and advances the current position within this stream by the number of characters written.</span></span> <span data-ttu-id="cd944-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="cd944-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="cd944-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd944-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="cd944-106">Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="cd944-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="cd944-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd944-107">Parameters</span></span>

`buffer`  
<span data-ttu-id="cd944-108">Un tableau de caractères à écrire.</span><span class="sxs-lookup"><span data-stu-id="cd944-108">A char array to write.</span></span>

`offset`  
<span data-ttu-id="cd944-109">Un décalage relatif à l’origine.</span><span class="sxs-lookup"><span data-stu-id="cd944-109">An offset relative to origin.</span></span>

`count`  
<span data-ttu-id="cd944-110">Le nombre de caractères à écrire dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="cd944-110">The number of characters to be written to the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd944-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cd944-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="cd944-112">Le `SqlStreamChars.Write` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="cd944-112">The `SqlStreamChars.Write` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="cd944-113">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="cd944-113">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd944-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd944-114">Requirements</span></span>

<span data-ttu-id="cd944-115">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="cd944-115">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="cd944-116">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="cd944-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="cd944-117">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="cd944-117">**.NET Framework versions:** Available since 2.0.</span></span>
