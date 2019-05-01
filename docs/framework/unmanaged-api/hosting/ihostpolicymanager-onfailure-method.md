---
title: IHostPolicyManager::OnFailure, méthode
ms.date: 03/30/2017
api_name:
- IHostPolicyManager.OnFailure
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostPolicyManager::OnFailure
helpviewer_keywords:
- OnFailure method [.NET Framework hosting]
- IHostPolicyManager::OnFailure method [.NET Framework hosting]
ms.assetid: 77d3f31e-9a53-4349-9c02-610a71736d42
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 78d2b84598a034bf6c534745bcb99a080d039617
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993172"
---
# <a name="ihostpolicymanageronfailure-method"></a><span data-ttu-id="5c4cc-102">IHostPolicyManager::OnFailure, méthode</span><span class="sxs-lookup"><span data-stu-id="5c4cc-102">IHostPolicyManager::OnFailure Method</span></span>
<span data-ttu-id="5c4cc-103">Avertit l’hôte que le common language runtime (CLR) est sur le point d’effectuer l’action spécifiée par un appel à la [ICLRPolicyManager::SetActionOnFailure](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md) méthode en réponse à une ressource d’allocation ou un échec.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-103">Notifies the host that the common language runtime (CLR) is about to take the action specified by a call to the [ICLRPolicyManager::SetActionOnFailure](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md) method in response to a resource allocation or reclamation failure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c4cc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c4cc-104">Syntax</span></span>  
  
```  
HRESULT OnFailure(  
    [in] EClrFailure   failure,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c4cc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c4cc-105">Parameters</span></span>  
 `failure`  
 <span data-ttu-id="5c4cc-106">[in] Parmi les [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md) valeurs indiquant le genre d’échec auquel le CLR répond.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-106">[in] One of the [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md) values, indicating the kind of failure to which the CLR is responding.</span></span>  
  
 `action`  
 <span data-ttu-id="5c4cc-107">[in] Parmi les [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) valeurs, indiquant l’action, le CLR effectue en réponse à `failure`.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-107">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the action the CLR is taking in response to `failure`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5c4cc-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5c4cc-108">Return Value</span></span>  
  
|<span data-ttu-id="5c4cc-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5c4cc-109">HRESULT</span></span>|<span data-ttu-id="5c4cc-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c4cc-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5c4cc-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c4cc-111">S_OK</span></span>|<span data-ttu-id="5c4cc-112">`OnFailure` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-112">`OnFailure` returned successfully.</span></span>|  
|<span data-ttu-id="5c4cc-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="5c4cc-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="5c4cc-114">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="5c4cc-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5c4cc-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="5c4cc-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-116">The call timed out.</span></span>|  
|<span data-ttu-id="5c4cc-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="5c4cc-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="5c4cc-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="5c4cc-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="5c4cc-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="5c4cc-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="5c4cc-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="5c4cc-121">E_FAIL</span></span>|<span data-ttu-id="5c4cc-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="5c4cc-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="5c4cc-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="5c4cc-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5c4cc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c4cc-125">Requirements</span></span>  
 <span data-ttu-id="5c4cc-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5c4cc-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5c4cc-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5c4cc-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5c4cc-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5c4cc-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5c4cc-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5c4cc-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c4cc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c4cc-130">See also</span></span>

- [<span data-ttu-id="5c4cc-131">EClrFailure, énumération</span><span class="sxs-lookup"><span data-stu-id="5c4cc-131">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="5c4cc-132">EPolicyAction, énumération</span><span class="sxs-lookup"><span data-stu-id="5c4cc-132">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)
- [<span data-ttu-id="5c4cc-133">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="5c4cc-133">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [<span data-ttu-id="5c4cc-134">IHostPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="5c4cc-134">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
