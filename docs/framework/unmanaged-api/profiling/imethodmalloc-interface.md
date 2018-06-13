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
ms.openlocfilehash: b11cf0fadc9142ee291115cf9f0d84e6429834fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455115"
---
# <a name="imethodmalloc-interface"></a><span data-ttu-id="d841c-102">IMethodMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="d841c-102">IMethodMalloc Interface</span></span>
<span data-ttu-id="d841c-103">Fournit une méthode pour allouer de la mémoire pour un nouveau corps de fonction MSIL (intermediate language).</span><span class="sxs-lookup"><span data-stu-id="d841c-103">Provides a method to allocate memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d841c-104">Le `IMethodMalloc` interface est un allocateur de mémoire simple.</span><span class="sxs-lookup"><span data-stu-id="d841c-104">The `IMethodMalloc` interface is a simple memory allocator.</span></span> <span data-ttu-id="d841c-105">Elle permet à allouer de la mémoire, mais ne pas pour le libérer.</span><span class="sxs-lookup"><span data-stu-id="d841c-105">It allows you to allocate memory, but not to free it.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d841c-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d841c-106">Methods</span></span>  
  
|<span data-ttu-id="d841c-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="d841c-107">Method</span></span>|<span data-ttu-id="d841c-108">Description</span><span class="sxs-lookup"><span data-stu-id="d841c-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d841c-109">Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="d841c-109">Alloc Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-alloc-method.md)|<span data-ttu-id="d841c-110">Tente d’allouer une quantité de mémoire spécifiée pour un nouveau corps de fonction MSIL.</span><span class="sxs-lookup"><span data-stu-id="d841c-110">Attempts to allocate a specified amount of memory for a new MSIL function body.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d841c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d841c-111">Remarks</span></span>  
 <span data-ttu-id="d841c-112">Chaque allocateur est spécifique au module et garantit que le corps de fonction sera à un offset positif à partir de la base du module.</span><span class="sxs-lookup"><span data-stu-id="d841c-112">Each allocator is module-specific and ensures that the function body will be at a positive offset from the base of the module.</span></span> <span data-ttu-id="d841c-113">Mémoire au-dessus de la base d’un module peut être précieuse, donc l’allocateur doit être utilisé pour allouer de la mémoire uniquement pour un corps de fonction.</span><span class="sxs-lookup"><span data-stu-id="d841c-113">Memory above the base of a module can be precious, so the allocator should be used to allocate memory only for a function body.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d841c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d841c-114">Requirements</span></span>  
 <span data-ttu-id="d841c-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d841c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d841c-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d841c-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d841c-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d841c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d841c-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d841c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d841c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d841c-119">See Also</span></span>  
 [<span data-ttu-id="d841c-120">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="d841c-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
