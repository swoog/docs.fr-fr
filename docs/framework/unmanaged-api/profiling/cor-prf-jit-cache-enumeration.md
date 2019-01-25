---
title: COR_PRF_JIT_CACHE, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_JIT_CACHE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_JIT_CACHE
helpviewer_keywords:
- COR_PRF_JIT_CACHE enumeration [.NET Framework profiling]
ms.assetid: e7b8f6b4-95bc-4ba5-b9eb-f5590a7326a4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6aaa334c83aff18886c0c2db4462d6baaa4cd70f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687412"
---
# <a name="corprfjitcache-enumeration"></a><span data-ttu-id="148b7-102">COR_PRF_JIT_CACHE, énumération</span><span class="sxs-lookup"><span data-stu-id="148b7-102">COR_PRF_JIT_CACHE Enumeration</span></span>
<span data-ttu-id="148b7-103">Indique le résultat de la recherche d'une fonction mise en cache.</span><span class="sxs-lookup"><span data-stu-id="148b7-103">Indicates the result of a cached function search.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="148b7-104">`COR_PRF_CACHED_FUNCTION_FOUND` a la valeur zéro, par conséquent, `COR_PRF_JIT_CACHE` ne peut pas être utilisé comme un substitut booléen.</span><span class="sxs-lookup"><span data-stu-id="148b7-104">`COR_PRF_CACHED_FUNCTION_FOUND` has a value of zero, so `COR_PRF_JIT_CACHE` cannot be used as a Boolean surrogate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="148b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="148b7-105">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_CACHED_FUNCTION_FOUND,  
    COR_PRF_CACHED_FUNCTION_NOT_FOUND  
} COR_PRF_JIT_CACHE;  
```  
  
## <a name="members"></a><span data-ttu-id="148b7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="148b7-106">Members</span></span>  
  
|<span data-ttu-id="148b7-107">Membre</span><span class="sxs-lookup"><span data-stu-id="148b7-107">Member</span></span>|<span data-ttu-id="148b7-108">Description</span><span class="sxs-lookup"><span data-stu-id="148b7-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FUNCTION_FOUND`|<span data-ttu-id="148b7-109">La recherche a trouvé la fonction.</span><span class="sxs-lookup"><span data-stu-id="148b7-109">The search found the function.</span></span>|  
|`COR_PRF_FUNCTION_NOT_FOUND`|<span data-ttu-id="148b7-110">La recherche ne n’a pas trouvé la fonction.</span><span class="sxs-lookup"><span data-stu-id="148b7-110">The search did not find the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="148b7-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="148b7-111">Requirements</span></span>  
 <span data-ttu-id="148b7-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="148b7-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="148b7-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="148b7-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="148b7-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="148b7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="148b7-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="148b7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="148b7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="148b7-116">See also</span></span>
- [<span data-ttu-id="148b7-117">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="148b7-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
