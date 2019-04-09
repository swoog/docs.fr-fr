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
ms.openlocfilehash: 54abd54662d4e99881dddf15876b596a4a705f70
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108899"
---
# <a name="iclroneventmanagerunregisteractiononevent-method"></a><span data-ttu-id="17aeb-102">ICLROnEventManager::UnregisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="17aeb-102">ICLROnEventManager::UnregisterActionOnEvent Method</span></span>
<span data-ttu-id="17aeb-103">Annule l’inscription d’un pointeur de rappel précédemment enregistré pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="17aeb-103">Unregisters a previously registered callback pointer for the specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17aeb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17aeb-104">Syntax</span></span>  
  
```  
HRESULT UnregisterActionOnEvent (  
    [in] EClrEvent event,  
    [in] IActionOnCLREvent *pAction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17aeb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17aeb-105">Parameters</span></span>  
 `event`  
 <span data-ttu-id="17aeb-106">[in] Parmi les [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) valeurs indiquant l’événement pour lequel annuler l’enregistrement du pointeur de rappel décrit par `pAction`.</span><span class="sxs-lookup"><span data-stu-id="17aeb-106">[in] One of the [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) values, indicating the event for which to unregister the callback pointer described by `pAction`.</span></span>  
  
 `pAction`  
 <span data-ttu-id="17aeb-107">[in] Un pointeur vers un [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) objet passé en tant que paramètre à la [RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="17aeb-107">[in] A pointer to an [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) object that was passed as a parameter to the [RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="17aeb-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="17aeb-108">Return Value</span></span>  
  
|<span data-ttu-id="17aeb-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="17aeb-109">HRESULT</span></span>|<span data-ttu-id="17aeb-110">Description</span><span class="sxs-lookup"><span data-stu-id="17aeb-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="17aeb-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="17aeb-111">S_OK</span></span>|`UnregisterActionOnEvent` <span data-ttu-id="17aeb-112">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="17aeb-112">returned successfully.</span></span>|  
|<span data-ttu-id="17aeb-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="17aeb-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="17aeb-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="17aeb-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="17aeb-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="17aeb-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="17aeb-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="17aeb-116">The call timed out.</span></span>|  
|<span data-ttu-id="17aeb-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="17aeb-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="17aeb-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="17aeb-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="17aeb-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="17aeb-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="17aeb-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="17aeb-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="17aeb-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="17aeb-121">E_FAIL</span></span>|<span data-ttu-id="17aeb-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="17aeb-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="17aeb-123">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="17aeb-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="17aeb-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="17aeb-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="17aeb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17aeb-125">Requirements</span></span>  
 <span data-ttu-id="17aeb-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="17aeb-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17aeb-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="17aeb-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="17aeb-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="17aeb-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="17aeb-129">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="17aeb-129">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="17aeb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17aeb-130">See also</span></span>

- [<span data-ttu-id="17aeb-131">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="17aeb-131">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)
- [<span data-ttu-id="17aeb-132">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="17aeb-132">IActionOnCLREvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md)
- [<span data-ttu-id="17aeb-133">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="17aeb-133">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="17aeb-134">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="17aeb-134">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
