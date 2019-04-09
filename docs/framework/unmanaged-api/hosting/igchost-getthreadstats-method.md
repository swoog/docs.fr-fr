---
title: IGCHost::GetThreadStats, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.GetThreadStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetThreadStats
helpviewer_keywords:
- IGCHost::GetThreadStats method [.NET Framework hosting]
- GetThreadStats method [.NET Framework hosting]
ms.assetid: 826baa9b-9218-4736-a509-7ab193b125a0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 88f86385ba4f4186d14994a2028ee11c42127546
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108345"
---
# <a name="igchostgetthreadstats-method"></a><span data-ttu-id="b722f-102">IGCHost::GetThreadStats, méthode</span><span class="sxs-lookup"><span data-stu-id="b722f-102">IGCHost::GetThreadStats Method</span></span>
<span data-ttu-id="b722f-103">Obtient les statistiques par thread pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="b722f-103">Gets the per-thread statistics for garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b722f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b722f-104">Syntax</span></span>  
  
```  
HRESULT GetThreadStats (  
    [in] DWORD *pFiberCookie,  
    [in, out] COR_GC_THREAD_STATS *pStats  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b722f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b722f-105">Parameters</span></span>  
 `pFiberCookie`  
 <span data-ttu-id="b722f-106">[in] Pointeur vers un cookie fiber qui spécifie le thread pour lequel récupérer les statistiques.</span><span class="sxs-lookup"><span data-stu-id="b722f-106">[in] A pointer to a fiber cookie that specifies the thread for which to retrieve the statistics.</span></span>  
  
 `pStats`  
 <span data-ttu-id="b722f-107">[in, out] Un pointeur vers un [COR_GC_THREAD_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-thread-stats-structure.md) structure qui contient les statistiques de garbage collection pour le thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="b722f-107">[in, out] A pointer to a [COR_GC_THREAD_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-thread-stats-structure.md) structure that contains the garbage collection statistics for the specified thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b722f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b722f-108">Requirements</span></span>  
 <span data-ttu-id="b722f-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b722f-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b722f-110">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="b722f-110">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="b722f-111">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b722f-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="b722f-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b722f-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b722f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b722f-113">See also</span></span>

- [<span data-ttu-id="b722f-114">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="b722f-114">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
