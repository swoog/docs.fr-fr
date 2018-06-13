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
ms.openlocfilehash: c3e0d6f68ffa5280d4616d4fa4ac60b4cb86f6a4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437763"
---
# <a name="igchostgetstats-method"></a><span data-ttu-id="8694a-102">IGCHost::GetStats, méthode</span><span class="sxs-lookup"><span data-stu-id="8694a-102">IGCHost::GetStats Method</span></span>
<span data-ttu-id="8694a-103">Obtient les statistiques de l’état actuel du système de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="8694a-103">Gets the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8694a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8694a-104">Syntax</span></span>  
  
```  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8694a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8694a-105">Parameters</span></span>  
 `pStats`  
 <span data-ttu-id="8694a-106">[dans, out] Un pointeur vers un [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure qui contient les statistiques de l’état actuel du système de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="8694a-106">[in, out] A pointer to a [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure that contains the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8694a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8694a-107">Remarks</span></span>  
 <span data-ttu-id="8694a-108">Les statistiques peuvent être utilisées par un système intelligent d’allocation pour utiliser le système de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="8694a-108">The statistics can be used by a smart allocation system to help the garbage collection system operate.</span></span> <span data-ttu-id="8694a-109">Par exemple, le système d’allocation peut déterminer, après avoir examiné les statistiques, il doit ajouter davantage de mémoire ou forcer une collection.</span><span class="sxs-lookup"><span data-stu-id="8694a-109">For example, the allocation system may determine, after reviewing the statistics, that it needs to add more memory or force a collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8694a-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8694a-110">Requirements</span></span>  
 <span data-ttu-id="8694a-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8694a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8694a-112">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="8694a-112">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="8694a-113">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8694a-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8694a-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8694a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8694a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8694a-115">See Also</span></span>  
 [<span data-ttu-id="8694a-116">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="8694a-116">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
