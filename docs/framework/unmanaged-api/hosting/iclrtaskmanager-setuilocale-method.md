---
title: ICLRTaskManager::SetUILocale, méthode
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.SetUILocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::SetUILocale
helpviewer_keywords:
- ICLRTaskManager::SetUILocale method [.NET Framework hosting]
- SetUILocale method, ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 03adaa9a-2beb-49b3-b2c4-6b4fc3f10715
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8ef939f915062368d74a0c48bdaee47cbec7b56f
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57491462"
---
# <a name="iclrtaskmanagersetuilocale-method"></a><span data-ttu-id="752f3-102">ICLRTaskManager::SetUILocale, méthode</span><span class="sxs-lookup"><span data-stu-id="752f3-102">ICLRTaskManager::SetUILocale Method</span></span>
<span data-ttu-id="752f3-103">Avertit le common language runtime (CLR) que l’hôte a modifié les paramètres régionaux de l’interface (UI) utilisateur ou la culture, à la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="752f3-103">Notifies the common language runtime (CLR) that the host has modified the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="752f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="752f3-104">Syntax</span></span>  
  
```  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="752f3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="752f3-105">Parameters</span></span>  
 `lcid`  
 <span data-ttu-id="752f3-106">[in] La valeur d’identificateur de paramètres régionaux qui mappe à la culture géographique qui vient d’être attribué et la langue pour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="752f3-106">[in] The locale identifier value that maps to the newly assigned geographical culture and language for the user interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="752f3-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="752f3-107">Return Value</span></span>  
  
|<span data-ttu-id="752f3-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="752f3-108">HRESULT</span></span>|<span data-ttu-id="752f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="752f3-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="752f3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="752f3-110">S_OK</span></span>|<span data-ttu-id="752f3-111">`SetUILocale` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="752f3-111">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="752f3-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="752f3-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="752f3-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="752f3-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="752f3-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="752f3-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="752f3-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="752f3-115">The call timed out.</span></span>|  
|<span data-ttu-id="752f3-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="752f3-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="752f3-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="752f3-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="752f3-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="752f3-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="752f3-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="752f3-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="752f3-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="752f3-120">E_FAIL</span></span>|<span data-ttu-id="752f3-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="752f3-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="752f3-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="752f3-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="752f3-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="752f3-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="752f3-124">Notes</span><span class="sxs-lookup"><span data-stu-id="752f3-124">Remarks</span></span>  
 <span data-ttu-id="752f3-125">`SetUILocale` Fournit une opportunité pour l’hôte exécuter des mécanismes qu'est peut-être pour la synchronisation des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="752f3-125">`SetUILocale` provides an opportunity for the host to execute any mechanisms it might have for the synchronization of locales.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="752f3-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="752f3-126">Requirements</span></span>  
 <span data-ttu-id="752f3-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="752f3-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="752f3-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="752f3-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="752f3-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="752f3-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="752f3-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="752f3-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="752f3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="752f3-131">See also</span></span>
- [<span data-ttu-id="752f3-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="752f3-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="752f3-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="752f3-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="752f3-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="752f3-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="752f3-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="752f3-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
