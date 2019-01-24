---
title: ICLRRuntimeHost::SetHostControl, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.SetHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::SetHostControl
helpviewer_keywords:
- SetHostControl method [.NET Framework hosting]
- ICLRRuntimeHost::SetHostControl method [.NET Framework hosting]
ms.assetid: 6136be87-e631-4756-81ed-74b66581bad4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e385744f1a9ecef2cbe1f6074501061dc2f15fe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602258"
---
# <a name="iclrruntimehostsethostcontrol-method"></a><span data-ttu-id="9f341-102">ICLRRuntimeHost::SetHostControl, méthode</span><span class="sxs-lookup"><span data-stu-id="9f341-102">ICLRRuntimeHost::SetHostControl Method</span></span>
<span data-ttu-id="9f341-103">Définit le pointeur d’interface que le common language runtime (CLR) peut utiliser pour obtenir l’implémentation de l’hôte de [IHostControl, Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9f341-103">Sets the interface pointer that the common language runtime (CLR) can use to get the host's implementation of [IHostControl Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f341-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f341-104">Syntax</span></span>  
  
```  
HRESULT SetHostControl(  
    [in] IHostControl* pHostControl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f341-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f341-105">Parameters</span></span>  
 `pHostControl`  
 <span data-ttu-id="9f341-106">[in] Pointeur d’interface vers l’implémentation de l’hôte de [IHostControl, Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9f341-106">[in] An interface pointer to the host's implementation of [IHostControl Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9f341-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9f341-107">Return Value</span></span>  
  
|<span data-ttu-id="9f341-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9f341-108">HRESULT</span></span>|<span data-ttu-id="9f341-109">Description</span><span class="sxs-lookup"><span data-stu-id="9f341-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9f341-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f341-110">S_OK</span></span>|<span data-ttu-id="9f341-111">`SetHostControl` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="9f341-111">`SetHostControl` returned successfully.</span></span>|  
|<span data-ttu-id="9f341-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9f341-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9f341-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="9f341-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="9f341-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9f341-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="9f341-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="9f341-115">The call timed out.</span></span>|  
|<span data-ttu-id="9f341-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="9f341-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="9f341-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="9f341-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="9f341-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="9f341-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="9f341-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="9f341-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="9f341-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9f341-120">E_FAIL</span></span>|<span data-ttu-id="9f341-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9f341-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="9f341-122">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="9f341-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="9f341-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="9f341-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="9f341-124">E_CLR_ALREADY_STARTED</span><span class="sxs-lookup"><span data-stu-id="9f341-124">E_CLR_ALREADY_STARTED</span></span>|<span data-ttu-id="9f341-125">Le CLR a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="9f341-125">The CLR has already been initialized.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9f341-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9f341-126">Remarks</span></span>  
 <span data-ttu-id="9f341-127">Vous devez appeler `SetHostControl` avant que le CLR est initialisé, autrement dit, avant d’appeler [méthode Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) ou utiliser une de la [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9f341-127">You must call `SetHostControl` before the CLR is initialized, that is, before you call [Start Method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) or use any of the [Metadata Interfaces](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span></span> <span data-ttu-id="9f341-128">Il est recommandé d’appeler `SetHostControl` immédiatement après l’appel [CorBindToCurrentRuntime, fonction](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md) ou [fonction CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f341-128">It is recommended that you call `SetHostControl` immediately after calling [CorBindToCurrentRuntime Function](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md) or [CorBindToRuntimeEx Function](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f341-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f341-129">Requirements</span></span>  
 <span data-ttu-id="9f341-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9f341-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f341-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9f341-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9f341-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f341-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9f341-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f341-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f341-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f341-134">See also</span></span>
- [<span data-ttu-id="9f341-135">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="9f341-135">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
- [<span data-ttu-id="9f341-136">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="9f341-136">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
