---
title: IHostSecurityManager::RevertToSelf, méthode
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.RevertToSelf
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::RevertToSelf
helpviewer_keywords:
- RevertToSelf method [.NET Framework hosting]
- IHostSecurityManager::RevertToSelf method [.NET Framework hosting]
ms.assetid: 189f28f8-f9a1-4192-aedc-91084e4f8b99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d282f6d37a2be8a41f4fbda579b3b467b9bfc8ca
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120066"
---
# <a name="ihostsecuritymanagerreverttoself-method"></a><span data-ttu-id="4a73b-102">IHostSecurityManager::RevertToSelf, méthode</span><span class="sxs-lookup"><span data-stu-id="4a73b-102">IHostSecurityManager::RevertToSelf Method</span></span>
<span data-ttu-id="4a73b-103">Termine l’emprunt d’identité de l’utilisateur actuel et retourne le jeton de thread d’origine.</span><span class="sxs-lookup"><span data-stu-id="4a73b-103">Terminates impersonation of the current user identity and returns the original thread token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a73b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a73b-104">Syntax</span></span>  
  
```  
HRESULT RevertToSelf ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="4a73b-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4a73b-105">Return Value</span></span>  
  
|<span data-ttu-id="4a73b-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a73b-106">HRESULT</span></span>|<span data-ttu-id="4a73b-107">Description</span><span class="sxs-lookup"><span data-stu-id="4a73b-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4a73b-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a73b-108">S_OK</span></span>|<span data-ttu-id="4a73b-109">`RevertToSelf` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="4a73b-109">`RevertToSelf` returned successfully.</span></span>|  
|<span data-ttu-id="4a73b-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="4a73b-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="4a73b-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="4a73b-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="4a73b-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="4a73b-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="4a73b-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="4a73b-113">The call timed out.</span></span>|  
|<span data-ttu-id="4a73b-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="4a73b-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="4a73b-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="4a73b-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="4a73b-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="4a73b-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="4a73b-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="4a73b-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="4a73b-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="4a73b-118">E_FAIL</span></span>|<span data-ttu-id="4a73b-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4a73b-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="4a73b-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="4a73b-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="4a73b-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="4a73b-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4a73b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4a73b-122">Remarks</span></span>  
 <span data-ttu-id="4a73b-123">`RevertToSelf` est appelée pour retourner au jeton de thread d’origine, après un appel antérieur à la [ImpersonateLoggedOnUser](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="4a73b-123">`RevertToSelf` is called to return to the original thread token, after an earlier call to the [ImpersonateLoggedOnUser](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a73b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a73b-124">Requirements</span></span>  
 <span data-ttu-id="4a73b-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4a73b-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a73b-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4a73b-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4a73b-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4a73b-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4a73b-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a73b-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a73b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a73b-129">See also</span></span>

- [<span data-ttu-id="4a73b-130">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="4a73b-130">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)
- [<span data-ttu-id="4a73b-131">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="4a73b-131">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)
- [<span data-ttu-id="4a73b-132">ImpersonateLoggedOnUser, méthode</span><span class="sxs-lookup"><span data-stu-id="4a73b-132">ImpersonateLoggedOnUser Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md)
