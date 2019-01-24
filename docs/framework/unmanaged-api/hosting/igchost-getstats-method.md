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
ms.openlocfilehash: d9a3775f453cb432ce6b92d067f93ca54c329c06
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674178"
---
# <a name="igchostgetstats-method"></a><span data-ttu-id="188f6-102">IGCHost::GetStats, méthode</span><span class="sxs-lookup"><span data-stu-id="188f6-102">IGCHost::GetStats Method</span></span>
<span data-ttu-id="188f6-103">Obtient les statistiques pour l’état actuel du système garbage collection.</span><span class="sxs-lookup"><span data-stu-id="188f6-103">Gets the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="188f6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="188f6-104">Syntax</span></span>  
  
```  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="188f6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="188f6-105">Parameters</span></span>  
 `pStats`  
 <span data-ttu-id="188f6-106">[in, out] Un pointeur vers un [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure qui contient les statistiques de l’état actuel du système garbage collection.</span><span class="sxs-lookup"><span data-stu-id="188f6-106">[in, out] A pointer to a [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure that contains the statistics for the current state of the garbage collection system.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="188f6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="188f6-107">Remarks</span></span>  
 <span data-ttu-id="188f6-108">Les statistiques peuvent être utilisées par un système intelligent d’allocation pour aider le système de garbage collection à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="188f6-108">The statistics can be used by a smart allocation system to help the garbage collection system operate.</span></span> <span data-ttu-id="188f6-109">Par exemple, le système d’allocation peut déterminer, après avoir examiné les statistiques dont il a besoin pour ajouter davantage de mémoire ou de forcer une collection.</span><span class="sxs-lookup"><span data-stu-id="188f6-109">For example, the allocation system may determine, after reviewing the statistics, that it needs to add more memory or force a collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="188f6-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="188f6-110">Requirements</span></span>  
 <span data-ttu-id="188f6-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="188f6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="188f6-112">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="188f6-112">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="188f6-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="188f6-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="188f6-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="188f6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="188f6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="188f6-115">See also</span></span>
- [<span data-ttu-id="188f6-116">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="188f6-116">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
