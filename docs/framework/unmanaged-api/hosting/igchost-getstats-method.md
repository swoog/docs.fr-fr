---
title: IGCHost::GetStats, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.GetStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetStats
helpviewer_keywords:
- GetStats method, IGCHost interface [.NET Framework hosting]
- IGCHost::GetStats method [.NET Framework hosting]
ms.assetid: c4ae022c-46ac-4f19-9ddd-09b955f19412
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 14751b41809eeda5e6bd990fae368879d0f30492
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59227832"
---
# <a name="igchostgetstats-method"></a><span data-ttu-id="011b2-102">IGCHost::GetStats, méthode</span><span class="sxs-lookup"><span data-stu-id="011b2-102">IGCHost::GetStats Method</span></span>
<span data-ttu-id="011b2-103">Obtient les statistiques pour l’état actuel du système garbage collection.</span><span class="sxs-lookup"><span data-stu-id="011b2-103">Gets the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="011b2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="011b2-104">Syntax</span></span>  
  
```  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="011b2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="011b2-105">Parameters</span></span>  
 `pStats`  
 <span data-ttu-id="011b2-106">[in, out] Un pointeur vers un [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure qui contient les statistiques de l’état actuel du système garbage collection.</span><span class="sxs-lookup"><span data-stu-id="011b2-106">[in, out] A pointer to a [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure that contains the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="011b2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="011b2-107">Remarks</span></span>  
 <span data-ttu-id="011b2-108">Les statistiques peuvent être utilisées par un système intelligent d’allocation pour aider le système de garbage collection à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="011b2-108">The statistics can be used by a smart allocation system to help the garbage collection system operate.</span></span> <span data-ttu-id="011b2-109">Par exemple, le système d’allocation peut déterminer, après avoir examiné les statistiques dont il a besoin pour ajouter davantage de mémoire ou de forcer une collection.</span><span class="sxs-lookup"><span data-stu-id="011b2-109">For example, the allocation system may determine, after reviewing the statistics, that it needs to add more memory or force a collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="011b2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="011b2-110">Requirements</span></span>  
 <span data-ttu-id="011b2-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="011b2-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="011b2-112">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="011b2-112">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="011b2-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="011b2-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="011b2-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="011b2-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="011b2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="011b2-115">See also</span></span>

- [<span data-ttu-id="011b2-116">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="011b2-116">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
