---
title: IMethodMalloc, interface
ms.date: 03/30/2017
api_name:
- IMethodMalloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc
helpviewer_keywords:
- IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8c8ab5dc-557c-473a-82f2-6e403eca7dac
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ee825da1f3f0fd72a3b47b48783f0f344af99b65
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59077768"
---
# <a name="imethodmalloc-interface"></a><span data-ttu-id="1a9a8-102">IMethodMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="1a9a8-102">IMethodMalloc Interface</span></span>
<span data-ttu-id="1a9a8-103">Fournit une méthode pour allouer de la mémoire pour un nouveau corps de fonction Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="1a9a8-103">Provides a method to allocate memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1a9a8-104">Le `IMethodMalloc` interface est un allocateur de mémoire simple.</span><span class="sxs-lookup"><span data-stu-id="1a9a8-104">The `IMethodMalloc` interface is a simple memory allocator.</span></span> <span data-ttu-id="1a9a8-105">Il vous permet d’allocation de mémoire, mais ne pas à libérer.</span><span class="sxs-lookup"><span data-stu-id="1a9a8-105">It allows you to allocate memory, but not to free it.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1a9a8-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a9a8-106">Methods</span></span>  
  
|<span data-ttu-id="1a9a8-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a9a8-107">Method</span></span>|<span data-ttu-id="1a9a8-108">Description</span><span class="sxs-lookup"><span data-stu-id="1a9a8-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1a9a8-109">Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="1a9a8-109">Alloc Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-alloc-method.md)|<span data-ttu-id="1a9a8-110">Tente d’allouer une quantité de mémoire spécifiée pour un nouveau corps de fonction MSIL.</span><span class="sxs-lookup"><span data-stu-id="1a9a8-110">Attempts to allocate a specified amount of memory for a new MSIL function body.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a9a8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1a9a8-111">Remarks</span></span>  
 <span data-ttu-id="1a9a8-112">Chaque allocateur est spécifique au module et vous permet de garantir que le corps de fonction à un décalage positif à partir de la base du module.</span><span class="sxs-lookup"><span data-stu-id="1a9a8-112">Each allocator is module-specific and ensures that the function body will be at a positive offset from the base of the module.</span></span> <span data-ttu-id="1a9a8-113">Mémoire au-dessus de la base d’un module peut être précieuse, l’allocateur doit être utilisé pour allouer de la mémoire uniquement pour un corps de fonction.</span><span class="sxs-lookup"><span data-stu-id="1a9a8-113">Memory above the base of a module can be precious, so the allocator should be used to allocate memory only for a function body.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a9a8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a9a8-114">Requirements</span></span>  
 <span data-ttu-id="1a9a8-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1a9a8-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a9a8-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1a9a8-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1a9a8-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1a9a8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1a9a8-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a9a8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a9a8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a9a8-119">See also</span></span>

- [<span data-ttu-id="1a9a8-120">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="1a9a8-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
