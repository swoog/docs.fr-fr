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
ms.openlocfilehash: 0cdbe36403f830926d611ffdc655d82ea25ddeef
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61599089"
---
# <a name="corprfjitcache-enumeration"></a><span data-ttu-id="289d5-102">COR_PRF_JIT_CACHE, énumération</span><span class="sxs-lookup"><span data-stu-id="289d5-102">COR_PRF_JIT_CACHE Enumeration</span></span>
<span data-ttu-id="289d5-103">Indique le résultat de la recherche d'une fonction mise en cache.</span><span class="sxs-lookup"><span data-stu-id="289d5-103">Indicates the result of a cached function search.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="289d5-104">`COR_PRF_CACHED_FUNCTION_FOUND` a la valeur zéro, par conséquent, `COR_PRF_JIT_CACHE` ne peut pas être utilisé comme un substitut booléen.</span><span class="sxs-lookup"><span data-stu-id="289d5-104">`COR_PRF_CACHED_FUNCTION_FOUND` has a value of zero, so `COR_PRF_JIT_CACHE` cannot be used as a Boolean surrogate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="289d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="289d5-105">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_CACHED_FUNCTION_FOUND,  
    COR_PRF_CACHED_FUNCTION_NOT_FOUND  
} COR_PRF_JIT_CACHE;  
```  
  
## <a name="members"></a><span data-ttu-id="289d5-106">Membres</span><span class="sxs-lookup"><span data-stu-id="289d5-106">Members</span></span>  
  
|<span data-ttu-id="289d5-107">Membre</span><span class="sxs-lookup"><span data-stu-id="289d5-107">Member</span></span>|<span data-ttu-id="289d5-108">Description</span><span class="sxs-lookup"><span data-stu-id="289d5-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FUNCTION_FOUND`|<span data-ttu-id="289d5-109">La recherche a trouvé la fonction.</span><span class="sxs-lookup"><span data-stu-id="289d5-109">The search found the function.</span></span>|  
|`COR_PRF_FUNCTION_NOT_FOUND`|<span data-ttu-id="289d5-110">La recherche ne n’a pas trouvé la fonction.</span><span class="sxs-lookup"><span data-stu-id="289d5-110">The search did not find the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="289d5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="289d5-111">Requirements</span></span>  
 <span data-ttu-id="289d5-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="289d5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="289d5-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="289d5-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="289d5-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="289d5-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="289d5-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="289d5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="289d5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="289d5-116">See also</span></span>

- [<span data-ttu-id="289d5-117">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="289d5-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
