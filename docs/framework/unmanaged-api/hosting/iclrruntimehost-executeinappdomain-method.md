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
ms.openlocfilehash: 86348c35a023e22d10c4ad2e08f5cb1104b895a8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59165472"
---
# <a name="iclrruntimehostexecuteinappdomain-method"></a><span data-ttu-id="521d9-102">ICLRRuntimeHost::ExecuteInAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="521d9-102">ICLRRuntimeHost::ExecuteInAppDomain Method</span></span>
<span data-ttu-id="521d9-103">Spécifie le <xref:System.AppDomain> dans lequel exécuter le code managé spécifié.</span><span class="sxs-lookup"><span data-stu-id="521d9-103">Specifies the <xref:System.AppDomain> in which to execute the specified managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="521d9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="521d9-104">Syntax</span></span>  
  
```  
HRESULT ExecuteInAppDomain(  
    [in] DWORD AppDomainId,   
    [in] FExecuteInDomainCallback pCallback,   
    [in] void* cookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="521d9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="521d9-105">Parameters</span></span>  
 `AppDomainId`  
 <span data-ttu-id="521d9-106">[in] L’ID numérique de la <xref:System.AppDomain> dans lequel exécuter la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="521d9-106">[in] The numeric ID of the <xref:System.AppDomain> in which to execute the specified method.</span></span>  
  
 `pCallback`  
 <span data-ttu-id="521d9-107">[in] Un pointeur vers la fonction à exécuter dans le texte spécifié <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="521d9-107">[in] A pointer to the function to execute within the specified <xref:System.AppDomain>.</span></span>  
  
 `cookie`  
 <span data-ttu-id="521d9-108">[in] Un pointeur vers la mémoire allouée par l’appelant opaque.</span><span class="sxs-lookup"><span data-stu-id="521d9-108">[in] A pointer to opaque caller-allocated memory.</span></span> <span data-ttu-id="521d9-109">Ce paramètre est passé par le common language runtime (CLR) au rappel de domaine.</span><span class="sxs-lookup"><span data-stu-id="521d9-109">This parameter is passed by the common language runtime (CLR) to the domain callback.</span></span> <span data-ttu-id="521d9-110">Il n’est pas mémoire de tas géré par le runtime ; l’allocation et la durée de vie de cette mémoire sont contrôlées par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="521d9-110">It is not runtime-managed heap memory; both the allocation and lifetime of this memory are controlled by the caller.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="521d9-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="521d9-111">Return Value</span></span>  
  
|<span data-ttu-id="521d9-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="521d9-112">HRESULT</span></span>|<span data-ttu-id="521d9-113">Description</span><span class="sxs-lookup"><span data-stu-id="521d9-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="521d9-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="521d9-114">S_OK</span></span>|`ExecuteInAppDomain` <span data-ttu-id="521d9-115">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="521d9-115">returned successfully.</span></span>|  
|<span data-ttu-id="521d9-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="521d9-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="521d9-117">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="521d9-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="521d9-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="521d9-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="521d9-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="521d9-119">The call timed out.</span></span>|  
|<span data-ttu-id="521d9-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="521d9-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="521d9-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="521d9-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="521d9-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="521d9-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="521d9-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="521d9-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="521d9-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="521d9-124">E_FAIL</span></span>|<span data-ttu-id="521d9-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="521d9-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="521d9-126">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="521d9-126">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="521d9-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="521d9-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="521d9-128">Notes</span><span class="sxs-lookup"><span data-stu-id="521d9-128">Remarks</span></span>  
 `ExecuteInAppDomain` <span data-ttu-id="521d9-129">permet à l’hôte à exercer un contrôle sur lequel gérés <xref:System.AppDomain> la méthode managée spécifiée doit être exécutée dans.</span><span class="sxs-lookup"><span data-stu-id="521d9-129">allows the host to exercise control over which managed <xref:System.AppDomain> the specified managed method should be executed in.</span></span> <span data-ttu-id="521d9-130">Vous pouvez obtenir la valeur de l’identificateur d’un domaine d’application, ce qui correspond à la valeur de la <xref:System.AppDomain.Id%2A> propriété, en appelant [GetCurrentAppDomainId, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getcurrentappdomainid-method.md).</span><span class="sxs-lookup"><span data-stu-id="521d9-130">You can get the value of an application domain's identifier, which corresponds to the value of the <xref:System.AppDomain.Id%2A> property, by calling [GetCurrentAppDomainId Method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getcurrentappdomainid-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="521d9-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="521d9-131">Requirements</span></span>  
 <span data-ttu-id="521d9-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="521d9-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="521d9-133">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="521d9-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="521d9-134">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="521d9-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="521d9-135">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="521d9-135">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="521d9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="521d9-136">See also</span></span>

- [<span data-ttu-id="521d9-137">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="521d9-137">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
