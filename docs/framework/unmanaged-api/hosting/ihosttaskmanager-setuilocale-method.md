---
title: IHostTaskManager::SetUILocale, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.SetUILocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::SetUILocale
helpviewer_keywords:
- SetUILocale method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::SetUILocale method [.NET Framework hosting]
ms.assetid: d0c87a9c-ea81-4237-a16b-c22b36ec9dc8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e110f1f5ea326c232c7c96bb05913080e950083d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59158897"
---
# <a name="ihosttaskmanagersetuilocale-method"></a><span data-ttu-id="de0b6-102">IHostTaskManager::SetUILocale, méthode</span><span class="sxs-lookup"><span data-stu-id="de0b6-102">IHostTaskManager::SetUILocale Method</span></span>
<span data-ttu-id="de0b6-103">Avertit l’hôte que le common language runtime (CLR) a modifié les paramètres régionaux de l’interface (UI) utilisateur ou la culture, sur la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="de0b6-103">Notifies the host that the common language runtime (CLR) has changed the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de0b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de0b6-104">Syntax</span></span>  
  
```  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="de0b6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de0b6-105">Parameters</span></span>  
 `lcid`  
 <span data-ttu-id="de0b6-106">[in] La valeur d’identificateur de paramètres régionaux qui mappe à la culture géographique qui vient d’être attribué et la langue.</span><span class="sxs-lookup"><span data-stu-id="de0b6-106">[in] The locale identifier value that maps to the newly assigned geographical culture and language.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="de0b6-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="de0b6-107">Return Value</span></span>  
  
|<span data-ttu-id="de0b6-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="de0b6-108">HRESULT</span></span>|<span data-ttu-id="de0b6-109">Description</span><span class="sxs-lookup"><span data-stu-id="de0b6-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="de0b6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="de0b6-110">S_OK</span></span>|<span data-ttu-id="de0b6-111">`SetUILocale` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="de0b6-111">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="de0b6-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="de0b6-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="de0b6-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="de0b6-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="de0b6-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="de0b6-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="de0b6-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="de0b6-115">The call timed out.</span></span>|  
|<span data-ttu-id="de0b6-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="de0b6-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="de0b6-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="de0b6-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="de0b6-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="de0b6-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="de0b6-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="de0b6-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="de0b6-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="de0b6-120">E_FAIL</span></span>|<span data-ttu-id="de0b6-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="de0b6-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="de0b6-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="de0b6-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="de0b6-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="de0b6-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="de0b6-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="de0b6-124">E_NOTIMPL</span></span>|<span data-ttu-id="de0b6-125">L’hôte n’autorise pas de code utilisateur managé de modifier la culture d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="de0b6-125">The host does not allow managed user code to change the UI culture.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="de0b6-126">Notes</span><span class="sxs-lookup"><span data-stu-id="de0b6-126">Remarks</span></span>  
 <span data-ttu-id="de0b6-127">Le runtime appelle `SetUILocale` lorsque la valeur de la <xref:System.Threading.Thread.CurrentUICulture%2A?displayProperty=nameWithType> propriété est modifiée par le code managé.</span><span class="sxs-lookup"><span data-stu-id="de0b6-127">The runtime calls `SetUILocale` when the value of the <xref:System.Threading.Thread.CurrentUICulture%2A?displayProperty=nameWithType> property is changed by managed code.</span></span> <span data-ttu-id="de0b6-128">Cette méthode fournit une opportunité pour l’hôte exécuter des mécanismes qu'est peut-être pour la synchronisation des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="de0b6-128">This method provides an opportunity for the host to execute any mechanisms it might have for synchronization of locales.</span></span> <span data-ttu-id="de0b6-129">Si un ordinateur hôte n’autorise pas les paramètres régionaux de l’interface utilisateur à partir de code managé ou n’implémente pas de mécanisme pour synchroniser les paramètres régionaux, il doit retourner E_NOTIMPL à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="de0b6-129">If a host does not allow the UI locale to be changed from managed code, or does not implement a mechanism to synchronize locales, it should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de0b6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de0b6-130">Requirements</span></span>  
 <span data-ttu-id="de0b6-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="de0b6-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de0b6-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="de0b6-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="de0b6-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="de0b6-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="de0b6-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de0b6-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de0b6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de0b6-135">See also</span></span>

- [<span data-ttu-id="de0b6-136">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="de0b6-136">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="de0b6-137">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="de0b6-137">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="de0b6-138">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="de0b6-138">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="de0b6-139">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="de0b6-139">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="de0b6-140">SetLocale, méthode</span><span class="sxs-lookup"><span data-stu-id="de0b6-140">SetLocale Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-setlocale-method.md)
