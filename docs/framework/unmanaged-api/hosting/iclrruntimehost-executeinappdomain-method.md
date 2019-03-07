---
title: ICLRRuntimeHost::ExecuteInAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteInAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteInAppDomain
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteInAppDomain method [.NET Framework hosting]
- ExecuteInAppDomain method [.NET Framework hosting]
ms.assetid: e2b0e2db-3fae-4b56-844e-d30a125a660c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f4d59b3857b9c23ccb61e22319ffd2b3129bd26a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474846"
---
# <a name="iclrruntimehostexecuteinappdomain-method"></a><span data-ttu-id="e3d25-102">ICLRRuntimeHost::ExecuteInAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="e3d25-102">ICLRRuntimeHost::ExecuteInAppDomain Method</span></span>
<span data-ttu-id="e3d25-103">Spécifie le <xref:System.AppDomain> dans lequel exécuter le code managé spécifié.</span><span class="sxs-lookup"><span data-stu-id="e3d25-103">Specifies the <xref:System.AppDomain> in which to execute the specified managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3d25-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3d25-104">Syntax</span></span>  
  
```  
HRESULT ExecuteInAppDomain(  
    [in] DWORD AppDomainId,   
    [in] FExecuteInDomainCallback pCallback,   
    [in] void* cookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e3d25-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3d25-105">Parameters</span></span>  
 `AppDomainId`  
 <span data-ttu-id="e3d25-106">[in] L’ID numérique de la <xref:System.AppDomain> dans lequel exécuter la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e3d25-106">[in] The numeric ID of the <xref:System.AppDomain> in which to execute the specified method.</span></span>  
  
 `pCallback`  
 <span data-ttu-id="e3d25-107">[in] Un pointeur vers la fonction à exécuter dans le texte spécifié <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="e3d25-107">[in] A pointer to the function to execute within the specified <xref:System.AppDomain>.</span></span>  
  
 `cookie`  
 <span data-ttu-id="e3d25-108">[in] Un pointeur vers la mémoire allouée par l’appelant opaque.</span><span class="sxs-lookup"><span data-stu-id="e3d25-108">[in] A pointer to opaque caller-allocated memory.</span></span> <span data-ttu-id="e3d25-109">Ce paramètre est passé par le common language runtime (CLR) au rappel de domaine.</span><span class="sxs-lookup"><span data-stu-id="e3d25-109">This parameter is passed by the common language runtime (CLR) to the domain callback.</span></span> <span data-ttu-id="e3d25-110">Il n’est pas mémoire de tas géré par le runtime ; l’allocation et la durée de vie de cette mémoire sont contrôlées par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e3d25-110">It is not runtime-managed heap memory; both the allocation and lifetime of this memory are controlled by the caller.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e3d25-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e3d25-111">Return Value</span></span>  
  
|<span data-ttu-id="e3d25-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e3d25-112">HRESULT</span></span>|<span data-ttu-id="e3d25-113">Description</span><span class="sxs-lookup"><span data-stu-id="e3d25-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e3d25-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3d25-114">S_OK</span></span>|<span data-ttu-id="e3d25-115">`ExecuteInAppDomain` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="e3d25-115">`ExecuteInAppDomain` returned successfully.</span></span>|  
|<span data-ttu-id="e3d25-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e3d25-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e3d25-117">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="e3d25-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e3d25-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e3d25-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e3d25-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="e3d25-119">The call timed out.</span></span>|  
|<span data-ttu-id="e3d25-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e3d25-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e3d25-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="e3d25-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e3d25-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e3d25-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e3d25-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="e3d25-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e3d25-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e3d25-124">E_FAIL</span></span>|<span data-ttu-id="e3d25-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e3d25-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e3d25-126">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="e3d25-126">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e3d25-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e3d25-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e3d25-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e3d25-128">Remarks</span></span>  
 <span data-ttu-id="e3d25-129">`ExecuteInAppDomain` permet à l’hôte à exercer un contrôle sur lequel gérés <xref:System.AppDomain> la méthode managée spécifiée doit être exécutée dans.</span><span class="sxs-lookup"><span data-stu-id="e3d25-129">`ExecuteInAppDomain` allows the host to exercise control over which managed <xref:System.AppDomain> the specified managed method should be executed in.</span></span> <span data-ttu-id="e3d25-130">Vous pouvez obtenir la valeur de l’identificateur d’un domaine d’application, ce qui correspond à la valeur de la <xref:System.AppDomain.Id%2A> propriété, en appelant [GetCurrentAppDomainId, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getcurrentappdomainid-method.md).</span><span class="sxs-lookup"><span data-stu-id="e3d25-130">You can get the value of an application domain's identifier, which corresponds to the value of the <xref:System.AppDomain.Id%2A> property, by calling [GetCurrentAppDomainId Method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getcurrentappdomainid-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3d25-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3d25-131">Requirements</span></span>  
 <span data-ttu-id="e3d25-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e3d25-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3d25-133">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e3d25-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e3d25-134">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e3d25-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e3d25-135">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3d25-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3d25-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3d25-136">See also</span></span>
- [<span data-ttu-id="e3d25-137">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="e3d25-137">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
