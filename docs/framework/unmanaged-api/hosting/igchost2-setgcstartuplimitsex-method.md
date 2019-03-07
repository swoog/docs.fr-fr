---
title: IGCHost2::SetGCStartupLimitsEx, méthode
ms.date: 03/30/2017
api_name:
- IGCHost2.SetGCStartupLimitsEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost2::SetGCStartupLimitsEx
helpviewer_keywords:
- IGCHost2::SetGCStartupLimitsEx method [.NET Framework hosting]
- SetGCStartupLimitsEx method, IGCHost2 interface [.NET Framework hosting]
ms.assetid: bba941c2-1c57-46d3-bbf5-5fb92700c490
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 69976110a227f95cf157b19b270f25cc3808246e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57484106"
---
# <a name="igchost2setgcstartuplimitsex-method"></a><span data-ttu-id="7e8fe-102">IGCHost2::SetGCStartupLimitsEx, méthode</span><span class="sxs-lookup"><span data-stu-id="7e8fe-102">IGCHost2::SetGCStartupLimitsEx Method</span></span>
<span data-ttu-id="7e8fe-103">Définit la taille du segment et la taille maximale pour la génération 0.</span><span class="sxs-lookup"><span data-stu-id="7e8fe-103">Sets the segment size and the maximum size for generation 0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e8fe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e8fe-104">Syntax</span></span>  
  
```  
HRESULT SetGCStartupLimitsEx (  
    [in] SIZE_T SegmentSize,  
    [in] SIZE_T MaxGen0Size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7e8fe-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e8fe-105">Parameters</span></span>  
 `SegmentSize`  
 <span data-ttu-id="7e8fe-106">[in] La taille du segment utilisé par le système de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="7e8fe-106">[in] The size of the segment used by the garbage collection system.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="7e8fe-107">[in] La taille maximale pour la génération 0.</span><span class="sxs-lookup"><span data-stu-id="7e8fe-107">[in] The maximum size for generation 0.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7e8fe-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7e8fe-108">Remarks</span></span>  
 <span data-ttu-id="7e8fe-109">Les valeurs qui `SetGCStartupLimitsEx` jeux peuvent être spécifiés uniquement avant le démarrage de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="7e8fe-109">The values that `SetGCStartupLimitsEx` sets can be specified only before the host is started.</span></span> <span data-ttu-id="7e8fe-110">Ces valeurs ne peuvent pas être modifiées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7e8fe-110">These values cannot be changed later.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e8fe-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7e8fe-111">Requirements</span></span>  
 <span data-ttu-id="7e8fe-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7e8fe-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e8fe-113">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="7e8fe-113">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="7e8fe-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7e8fe-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7e8fe-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e8fe-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e8fe-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e8fe-116">See also</span></span>
- [<span data-ttu-id="7e8fe-117">IGCHost2, interface</span><span class="sxs-lookup"><span data-stu-id="7e8fe-117">IGCHost2 Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost2-interface.md)
