---
title: ICorConfiguration::SetGCThreadControl, méthode
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetGCThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCThreadControl
helpviewer_keywords:
- ICorConfiguration::SetGCThreadControl method [.NET Framework hosting]
- SetGCThreadControl method [.NET Framework hosting]
ms.assetid: 72e38e61-3d56-4ae3-b8f6-0ab7922aaf11
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9da3c0ee081b81411d13dfcf9c8557c6bd4d3448
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437305"
---
# <a name="icorconfigurationsetgcthreadcontrol-method"></a><span data-ttu-id="4f4ee-102">ICorConfiguration::SetGCThreadControl, méthode</span><span class="sxs-lookup"><span data-stu-id="4f4ee-102">ICorConfiguration::SetGCThreadControl Method</span></span>
<span data-ttu-id="4f4ee-103">Définit l’interface de rappel pour la planification des threads pour les tâches non-runtime qui seraient sinon bloqués pour un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="4f4ee-103">Sets the callback interface for scheduling threads for non-runtime tasks that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f4ee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f4ee-104">Syntax</span></span>  
  
```  
HRESULT SetGCThreadControl (  
    [in] IGCThreadControl* pGCThreadControl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4f4ee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f4ee-105">Parameters</span></span>  
 `pGCThreadControl`  
 <span data-ttu-id="4f4ee-106">[in] Un pointeur vers un [IGCThreadControl](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md) objet qui avertit l’hôte sur la suspension des threads pour les tâches non-runtime.</span><span class="sxs-lookup"><span data-stu-id="4f4ee-106">[in] A pointer to an [IGCThreadControl](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md) object that notifies the host about the suspension of threads for non-runtime tasks.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4f4ee-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4f4ee-107">Remarks</span></span>  
 <span data-ttu-id="4f4ee-108">L’hôte peut choisir dans le [IGCThreadControl::ThreadIsBlockingForSuspension](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-threadisblockingforsuspension-method.md) rappel de replanifier un thread.</span><span class="sxs-lookup"><span data-stu-id="4f4ee-108">The host may choose within the [IGCThreadControl::ThreadIsBlockingForSuspension](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-threadisblockingforsuspension-method.md) callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f4ee-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4f4ee-109">Requirements</span></span>  
 <span data-ttu-id="4f4ee-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ee-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4f4ee-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4f4ee-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4f4ee-112">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4f4ee-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4f4ee-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4f4ee-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f4ee-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f4ee-114">See Also</span></span>  
 [<span data-ttu-id="4f4ee-115">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="4f4ee-115">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
