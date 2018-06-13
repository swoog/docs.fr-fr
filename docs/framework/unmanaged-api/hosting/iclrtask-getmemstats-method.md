---
title: ICLRTask::GetMemStats, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask.GetMemStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::GetMemStats
helpviewer_keywords:
- ICLRTask::GetMemStats method [.NET Framework hosting]
- GetMemStats method [.NET Framework hosting]
ms.assetid: c9e07657-1682-4c30-a336-f8658ff1a125
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d2284a311f8355b65f312112db9cddd458517b46
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433890"
---
# <a name="iclrtaskgetmemstats-method"></a><span data-ttu-id="8af94-102">ICLRTask::GetMemStats, méthode</span><span class="sxs-lookup"><span data-stu-id="8af94-102">ICLRTask::GetMemStats Method</span></span>
<span data-ttu-id="8af94-103">Obtient des informations sur l’utilisation de mémoire de statistiques relatives à la tâche qui en cours [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) représente l’instance.</span><span class="sxs-lookup"><span data-stu-id="8af94-103">Gets statistical memory usage information related to the task that the current [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8af94-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8af94-104">Syntax</span></span>  
  
```  
HRESULT GetMemStats (  
    [out] COR_GC_THREAD_STATS *pMemUsage  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8af94-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8af94-105">Parameters</span></span>  
 `pMemUsage`  
 <span data-ttu-id="8af94-106">[out] Un pointeur vers un [COR_GC_THREAD_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-thread-stats-structure.md) instance qui contient des détails sur l’utilisation de la mémoire de la tâche, y compris le nombre d’octets alloués.</span><span class="sxs-lookup"><span data-stu-id="8af94-106">[out] A pointer to a [COR_GC_THREAD_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-thread-stats-structure.md) instance that contains details about the memory usage of the task, including the number of bytes allocated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8af94-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8af94-107">Return Value</span></span>  
  
|<span data-ttu-id="8af94-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8af94-108">HRESULT</span></span>|<span data-ttu-id="8af94-109">Description</span><span class="sxs-lookup"><span data-stu-id="8af94-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8af94-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8af94-110">S_OK</span></span>|<span data-ttu-id="8af94-111">`GetMemStats` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="8af94-111">`GetMemStats` returned successfully.</span></span>|  
|<span data-ttu-id="8af94-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8af94-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8af94-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="8af94-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8af94-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8af94-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8af94-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="8af94-115">The call timed out.</span></span>|  
|<span data-ttu-id="8af94-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8af94-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8af94-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="8af94-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8af94-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8af94-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8af94-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="8af94-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8af94-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8af94-120">E_FAIL</span></span>|<span data-ttu-id="8af94-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8af94-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8af94-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="8af94-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8af94-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="8af94-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8af94-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8af94-124">Requirements</span></span>  
 <span data-ttu-id="8af94-125">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8af94-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8af94-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8af94-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8af94-127">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8af94-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8af94-128">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8af94-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8af94-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8af94-129">See Also</span></span>  
 [<span data-ttu-id="8af94-130">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="8af94-130">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="8af94-131">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="8af94-131">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="8af94-132">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="8af94-132">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="8af94-133">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="8af94-133">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
