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
ms.openlocfilehash: c34d9243e4ed7ed2492784154b157189c7d22cd2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440578"
---
# <a name="ihostsecuritymanagerreverttoself-method"></a><span data-ttu-id="da188-102">IHostSecurityManager::RevertToSelf, méthode</span><span class="sxs-lookup"><span data-stu-id="da188-102">IHostSecurityManager::RevertToSelf Method</span></span>
<span data-ttu-id="da188-103">Met fin à l’emprunt d’identité de l’utilisateur actuel et retourne le jeton de thread d’origine.</span><span class="sxs-lookup"><span data-stu-id="da188-103">Terminates impersonation of the current user identity and returns the original thread token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da188-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da188-104">Syntax</span></span>  
  
```  
HRESULT RevertToSelf ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="da188-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="da188-105">Return Value</span></span>  
  
|<span data-ttu-id="da188-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="da188-106">HRESULT</span></span>|<span data-ttu-id="da188-107">Description</span><span class="sxs-lookup"><span data-stu-id="da188-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="da188-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="da188-108">S_OK</span></span>|<span data-ttu-id="da188-109">`RevertToSelf` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="da188-109">`RevertToSelf` returned successfully.</span></span>|  
|<span data-ttu-id="da188-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="da188-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="da188-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="da188-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="da188-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="da188-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="da188-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="da188-113">The call timed out.</span></span>|  
|<span data-ttu-id="da188-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="da188-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="da188-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="da188-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="da188-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="da188-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="da188-117">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="da188-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="da188-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="da188-118">E_FAIL</span></span>|<span data-ttu-id="da188-119">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="da188-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="da188-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="da188-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="da188-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="da188-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="da188-122">Notes</span><span class="sxs-lookup"><span data-stu-id="da188-122">Remarks</span></span>  
 <span data-ttu-id="da188-123">`RevertToSelf` est appelée pour retourner au jeton de thread d’origine, après un appel antérieur à la [ImpersonateLoggedOnUser](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="da188-123">`RevertToSelf` is called to return to the original thread token, after an earlier call to the [ImpersonateLoggedOnUser](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da188-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="da188-124">Requirements</span></span>  
 <span data-ttu-id="da188-125">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="da188-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da188-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="da188-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="da188-127">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="da188-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="da188-128">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da188-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da188-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da188-129">See Also</span></span>  
 [<span data-ttu-id="da188-130">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="da188-130">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)  
 [<span data-ttu-id="da188-131">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="da188-131">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [<span data-ttu-id="da188-132">ImpersonateLoggedOnUser, méthode</span><span class="sxs-lookup"><span data-stu-id="da188-132">ImpersonateLoggedOnUser Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md)
