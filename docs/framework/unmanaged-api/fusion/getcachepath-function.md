---
title: GetCachePath, fonction
ms.date: 03/30/2017
api_name:
- GetCachePath
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- GetCachePath
helpviewer_keywords:
- GetCachePath function [.NET Framework fusion]
ms.assetid: d977ad29-6619-42e1-b0be-bc25ea950e80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cf23a8f1893aa0f992d554d3c7533c3dc42f4e95
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59150980"
---
# <a name="getcachepath-function"></a><span data-ttu-id="fb417-102">GetCachePath, fonction</span><span class="sxs-lookup"><span data-stu-id="fb417-102">GetCachePath Function</span></span>
<span data-ttu-id="fb417-103">Obtient le chemin d’accès à l’assembly mis en cache, à l’aide des indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fb417-103">Gets the path to the cached assembly, using the specified flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb417-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb417-104">Syntax</span></span>  
  
```  
HRESULT GetCachePath (  
    [in]      ASM_CACHE_FLAGS  dwCacheFlags,  
    [in]      LPWSTR           pwzCachePath,  
    [in, out] PDWORD           pcchPath  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="fb417-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb417-105">Parameters</span></span>  
 `dwCacheFlags`  
 <span data-ttu-id="fb417-106">[in] Un [ASM_CACHE_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md) valeur qui indique la source de l’assembly mis en cache.</span><span class="sxs-lookup"><span data-stu-id="fb417-106">[in] An [ASM_CACHE_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md) value that indicates the source of the cached assembly.</span></span>  
  
 `pwzCachePath`  
 <span data-ttu-id="fb417-107">[out] Le pointeur retourné pour le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="fb417-107">[out] The returned pointer to the path.</span></span>  
  
 `pcchPath`  
 <span data-ttu-id="fb417-108">[in, out] La longueur maximale demandée de `pwzCachePath`et au retour, la longueur réelle des `pwzCachePath`.</span><span class="sxs-lookup"><span data-stu-id="fb417-108">[in, out] The requested maximum length of `pwzCachePath`, and upon return, the actual length of `pwzCachePath`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb417-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb417-109">Requirements</span></span>  
 <span data-ttu-id="fb417-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fb417-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb417-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="fb417-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="fb417-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fb417-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb417-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb417-113">See also</span></span>

- [<span data-ttu-id="fb417-114">ASM_CACHE_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="fb417-114">ASM_CACHE_FLAGS Enumeration</span></span>](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md)
- [<span data-ttu-id="fb417-115">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="fb417-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
