---
title: IHostTask::Start, méthode
ms.date: 03/30/2017
api_name:
- IHostTask.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Start
helpviewer_keywords:
- IHostTask::Start method [.NET Framework hosting]
- Start method, IHostTask interface [.NET Framework hosting]
ms.assetid: b18742b0-d8c4-401c-ae89-e6eccdaa81d0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d45c5b09358430535438734b38e5dce5d1bcdd3e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59101625"
---
# <a name="ihosttaskstart-method"></a><span data-ttu-id="227ff-102">IHostTask::Start, méthode</span><span class="sxs-lookup"><span data-stu-id="227ff-102">IHostTask::Start Method</span></span>
<span data-ttu-id="227ff-103">Demande que l’hôte déplace la tâche représentée par l’actuel [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance à partir d’un suspendu à un état actif, dans lequel le code peut être exécuté.</span><span class="sxs-lookup"><span data-stu-id="227ff-103">Requests that the host move the task represented by the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance from a suspended to a live state, in which code can be executed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="227ff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="227ff-104">Syntax</span></span>  
  
```  
HRESULT Start ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="227ff-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="227ff-105">Return Value</span></span>  
  
|<span data-ttu-id="227ff-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="227ff-106">HRESULT</span></span>|<span data-ttu-id="227ff-107">Description</span><span class="sxs-lookup"><span data-stu-id="227ff-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="227ff-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="227ff-108">S_OK</span></span>|<span data-ttu-id="227ff-109">Start est retournée avec succès.</span><span class="sxs-lookup"><span data-stu-id="227ff-109">Start returned successfully.</span></span>|  
|<span data-ttu-id="227ff-110">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="227ff-110">E_FAIL</span></span>|<span data-ttu-id="227ff-111">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="227ff-111">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="227ff-112">Lorsqu’une méthode retourne E_FAIL, le common language runtime (CLR) n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="227ff-112">When a method returns E_FAIL, the common language runtime (CLR) is no longer usable within the process.</span></span> <span data-ttu-id="227ff-113">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="227ff-113">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="227ff-114">Notes</span><span class="sxs-lookup"><span data-stu-id="227ff-114">Remarks</span></span>  
 `Start` <span data-ttu-id="227ff-115">Retourne toujours une valeur HRESULT de S_OK, sauf dans les cas où une défaillance irrémédiable s’est produite.</span><span class="sxs-lookup"><span data-stu-id="227ff-115">always returns an HRESULT value of S_OK, except in cases where a catastrophic failure has occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="227ff-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="227ff-116">Requirements</span></span>  
 <span data-ttu-id="227ff-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="227ff-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="227ff-118">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="227ff-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="227ff-119">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="227ff-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="227ff-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="227ff-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="227ff-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="227ff-121">See also</span></span>

- [<span data-ttu-id="227ff-122">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="227ff-122">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="227ff-123">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="227ff-123">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="227ff-124">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="227ff-124">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="227ff-125">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="227ff-125">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
