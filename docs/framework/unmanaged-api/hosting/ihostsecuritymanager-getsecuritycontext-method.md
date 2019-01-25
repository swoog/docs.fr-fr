---
title: IHostSecurityManager::GetSecurityContext, méthode
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.GetSecurityContext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::GetSecurityContext
helpviewer_keywords:
- GetSecurityContext method [.NET Framework hosting]
- IHostSecurityManager::GetSecurityContext method [.NET Framework hosting]
ms.assetid: 958970d6-f6a2-4b84-b32a-f555cbaf8f61
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e11b447ebd03746730a86dbbcda31edd4196f13b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644948"
---
# <a name="ihostsecuritymanagergetsecuritycontext-method"></a><span data-ttu-id="f4af6-102">IHostSecurityManager::GetSecurityContext, méthode</span><span class="sxs-lookup"><span data-stu-id="f4af6-102">IHostSecurityManager::GetSecurityContext Method</span></span>
<span data-ttu-id="f4af6-103">Obtient le texte demandé [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f4af6-103">Gets the requested [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) from the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4af6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4af6-104">Syntax</span></span>  
  
```  
HRESULT GetSecurityContext (  
    [in]  EContextType eContextType,   
    [out] IHostSecurityContext** ppSecurityContext  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f4af6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4af6-105">Parameters</span></span>  
 `eContextType`  
 <span data-ttu-id="f4af6-106">[in] Parmi les [EContextType](../../../../docs/framework/unmanaged-api/hosting/econtexttype-enumeration.md) valeurs, indiquant le type du contexte de sécurité à retourner.</span><span class="sxs-lookup"><span data-stu-id="f4af6-106">[in] One of the [EContextType](../../../../docs/framework/unmanaged-api/hosting/econtexttype-enumeration.md) values, indicating what type of security context to return.</span></span>  
  
 `ppSecurityContext`  
 <span data-ttu-id="f4af6-107">[out] L’adresse du pointeur d’interface vers le `IHostSecurityContext` de `eContextType`.</span><span class="sxs-lookup"><span data-stu-id="f4af6-107">[out] The address of an interface pointer to the `IHostSecurityContext` of `eContextType`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f4af6-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f4af6-108">Return Value</span></span>  
  
|<span data-ttu-id="f4af6-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f4af6-109">HRESULT</span></span>|<span data-ttu-id="f4af6-110">Description</span><span class="sxs-lookup"><span data-stu-id="f4af6-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f4af6-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4af6-111">S_OK</span></span>|<span data-ttu-id="f4af6-112">`GetSecurityContext` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f4af6-112">`GetSecurityContext` returned successfully.</span></span>|  
|<span data-ttu-id="f4af6-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f4af6-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f4af6-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f4af6-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f4af6-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f4af6-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f4af6-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f4af6-116">The call timed out.</span></span>|  
|<span data-ttu-id="f4af6-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f4af6-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f4af6-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f4af6-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f4af6-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f4af6-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f4af6-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f4af6-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f4af6-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f4af6-121">E_FAIL</span></span>|<span data-ttu-id="f4af6-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f4af6-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f4af6-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="f4af6-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f4af6-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f4af6-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f4af6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f4af6-125">Remarks</span></span>  
 <span data-ttu-id="f4af6-126">Un hôte peut contrôler tous les accès de code aux jetons de thread par le code CLR et utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4af6-126">A host can control all code access to thread tokens by both the CLR and user code.</span></span> <span data-ttu-id="f4af6-127">Il peut également garantir que la sécurité complète des informations de contexte sont passées aux opérations asynchrones ou des points de code avec accès restreint au code.</span><span class="sxs-lookup"><span data-stu-id="f4af6-127">It can also ensure that complete security context information is passed across asynchronous operations or code points with restricted code access.</span></span> <span data-ttu-id="f4af6-128">`IHostSecurityContext` encapsule ces informations de contexte de sécurité, qui sont opaques pour le CLR.</span><span class="sxs-lookup"><span data-stu-id="f4af6-128">`IHostSecurityContext` encapsulates this security context information, which is opaque to the CLR.</span></span> <span data-ttu-id="f4af6-129">Le CLR collecte ces informations et les déplace dans la répartition d’élément de travail de pool de threads, l’exécution du finaliseur et la construction de module et de classe.</span><span class="sxs-lookup"><span data-stu-id="f4af6-129">The CLR captures this information and moves it across thread pool worker item dispatch, finalizer execution, and module and class construction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4af6-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f4af6-130">Requirements</span></span>  
 <span data-ttu-id="f4af6-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f4af6-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4af6-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f4af6-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f4af6-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f4af6-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f4af6-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4af6-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4af6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4af6-135">See also</span></span>
- [<span data-ttu-id="f4af6-136">EContextType, énumération</span><span class="sxs-lookup"><span data-stu-id="f4af6-136">EContextType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/econtexttype-enumeration.md)
- [<span data-ttu-id="f4af6-137">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="f4af6-137">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)
- [<span data-ttu-id="f4af6-138">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="f4af6-138">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)
