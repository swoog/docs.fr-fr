---
title: ICLRTaskManager::SetLocale, méthode
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.SetLocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::SetLocale
helpviewer_keywords:
- SetLocale method, ICLRTaskManager interface [.NET Framework hosting]
- ICLRTaskManager::SetLocale method [.NET Framework hosting]
ms.assetid: ed16bb7f-4206-43a8-b9e9-c5737b69e3af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ad9e07e76d39ce25dc339eb5fb02635866966093
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54612123"
---
# <a name="iclrtaskmanagersetlocale-method"></a><span data-ttu-id="0fe53-102">ICLRTaskManager::SetLocale, méthode</span><span class="sxs-lookup"><span data-stu-id="0fe53-102">ICLRTaskManager::SetLocale Method</span></span>
<span data-ttu-id="0fe53-103">Notifie le common language runtime (CLR) que l’hôte a modifié la valeur de l’identificateur de paramètres régionaux (qui est mappé à la culture géographique et la langue) sur la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0fe53-103">Notifies the common language runtime (CLR) that the host has modified the value of the locale identifier (which maps to the geographical culture and language) on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fe53-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fe53-104">Syntax</span></span>  
  
```  
HRESULT SetLocale (  
    [in] LCID lcid  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0fe53-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fe53-105">Parameters</span></span>  
 `lcid`  
 <span data-ttu-id="0fe53-106">[in] La valeur d’identificateur de paramètres régionaux qui mappe à la culture géographique qui vient d’être attribué et la langue.</span><span class="sxs-lookup"><span data-stu-id="0fe53-106">[in] The locale identifier value that maps to the newly assigned geographical culture and language.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0fe53-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0fe53-107">Return Value</span></span>  
  
|<span data-ttu-id="0fe53-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0fe53-108">HRESULT</span></span>|<span data-ttu-id="0fe53-109">Description</span><span class="sxs-lookup"><span data-stu-id="0fe53-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0fe53-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0fe53-110">S_OK</span></span>|<span data-ttu-id="0fe53-111">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="0fe53-111">The method returned successfully.</span></span>|  
|<span data-ttu-id="0fe53-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0fe53-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0fe53-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="0fe53-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0fe53-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0fe53-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0fe53-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="0fe53-115">The call timed out.</span></span>|  
|<span data-ttu-id="0fe53-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0fe53-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0fe53-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="0fe53-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0fe53-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0fe53-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0fe53-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="0fe53-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0fe53-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0fe53-120">E_FAIL</span></span>|<span data-ttu-id="0fe53-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0fe53-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0fe53-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="0fe53-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0fe53-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0fe53-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0fe53-124">Notes</span><span class="sxs-lookup"><span data-stu-id="0fe53-124">Remarks</span></span>  
 <span data-ttu-id="0fe53-125">`SetLocale` donne la possibilité d’exécuter n’importe quel mécanismes qu'est peut-être pour la synchronisation des paramètres régionaux de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="0fe53-125">`SetLocale` gives the host an opportunity to execute any mechanisms it might have for the synchronization of locales.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fe53-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0fe53-126">Requirements</span></span>  
 <span data-ttu-id="0fe53-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0fe53-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0fe53-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0fe53-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0fe53-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0fe53-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0fe53-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0fe53-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fe53-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fe53-131">See also</span></span>
- [<span data-ttu-id="0fe53-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="0fe53-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="0fe53-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="0fe53-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="0fe53-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="0fe53-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="0fe53-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="0fe53-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
