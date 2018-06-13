---
title: ICLROnEventManager::UnregisterActionOnEvent, méthode
ms.date: 03/30/2017
api_name:
- ICLROnEventManager.UnregisterActionOnEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager::UnregisterActionOnEvent
helpviewer_keywords:
- UnRegisterActionOnEvent method [.NET Framework hosting]
- ICLROnEventManager::UnRegisterActionOnEvent method [.NET Framework hosting]
ms.assetid: 4c02ec37-cdf0-46b2-890e-235092741236
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7add5e85aac273b4d513a24196af8305082c417f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434648"
---
# <a name="iclroneventmanagerunregisteractiononevent-method"></a><span data-ttu-id="cbd0f-102">ICLROnEventManager::UnregisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="cbd0f-102">ICLROnEventManager::UnregisterActionOnEvent Method</span></span>
<span data-ttu-id="cbd0f-103">Annule l’inscription d’un pointeur de rappel précédemment enregistré pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-103">Unregisters a previously registered callback pointer for the specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbd0f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbd0f-104">Syntax</span></span>  
  
```  
HRESULT UnregisterActionOnEvent (  
    [in] EClrEvent event,  
    [in] IActionOnCLREvent *pAction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cbd0f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbd0f-105">Parameters</span></span>  
 `event`  
 <span data-ttu-id="cbd0f-106">[in] Parmi les [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) indiquant l’événement pour lequel annuler l’enregistrement du pointeur de rappel décrit par les valeurs `pAction`.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-106">[in] One of the [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) values, indicating the event for which to unregister the callback pointer described by `pAction`.</span></span>  
  
 `pAction`  
 <span data-ttu-id="cbd0f-107">[in] Un pointeur vers un [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) objet qui a été passé en tant que paramètre à la [RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="cbd0f-107">[in] A pointer to an [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) object that was passed as a parameter to the [RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cbd0f-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cbd0f-108">Return Value</span></span>  
  
|<span data-ttu-id="cbd0f-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cbd0f-109">HRESULT</span></span>|<span data-ttu-id="cbd0f-110">Description</span><span class="sxs-lookup"><span data-stu-id="cbd0f-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cbd0f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbd0f-111">S_OK</span></span>|<span data-ttu-id="cbd0f-112">`UnregisterActionOnEvent` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-112">`UnregisterActionOnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="cbd0f-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cbd0f-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cbd0f-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cbd0f-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cbd0f-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cbd0f-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-116">The call timed out.</span></span>|  
|<span data-ttu-id="cbd0f-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cbd0f-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cbd0f-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cbd0f-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cbd0f-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cbd0f-120">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cbd0f-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cbd0f-121">E_FAIL</span></span>|<span data-ttu-id="cbd0f-122">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cbd0f-123">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cbd0f-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="cbd0f-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cbd0f-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cbd0f-125">Requirements</span></span>  
 <span data-ttu-id="cbd0f-126">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cbd0f-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cbd0f-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cbd0f-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cbd0f-128">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cbd0f-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cbd0f-129">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cbd0f-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cbd0f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbd0f-130">See Also</span></span>  
 [<span data-ttu-id="cbd0f-131">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="cbd0f-131">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)  
 [<span data-ttu-id="cbd0f-132">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="cbd0f-132">IActionOnCLREvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md)  
 [<span data-ttu-id="cbd0f-133">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="cbd0f-133">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="cbd0f-134">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="cbd0f-134">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
