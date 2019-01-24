---
title: ICLRRuntimeHost::GetCLRControl, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.GetCLRControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::GetCLRControl
helpviewer_keywords:
- ICLRRuntimeHost::GetCLRControl method [.NET Framework hosting]
- GetCLRControl method [.NET Framework hosting]
ms.assetid: e47e3655-efd5-4572-a1dc-50c69bf2a468
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8f426bac735c780d63b75eeaf49151651fd2fa65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692897"
---
# <a name="iclrruntimehostgetclrcontrol-method"></a><span data-ttu-id="8ef67-102">ICLRRuntimeHost::GetCLRControl, méthode</span><span class="sxs-lookup"><span data-stu-id="8ef67-102">ICLRRuntimeHost::GetCLRControl Method</span></span>
<span data-ttu-id="8ef67-103">Obtient un pointeur d’interface de type [ICLRControl, Interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md) que les hôtes peuvent utiliser pour personnaliser les aspects du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="8ef67-103">Gets an interface pointer of type [ICLRControl Interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md) that hosts can use to customize aspects of the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ef67-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ef67-104">Syntax</span></span>  
  
```  
HRESULT GetCLRControl(  
    [out] ICLRControl** pCLRControl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8ef67-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ef67-105">Parameters</span></span>  
 `pCLRControl`  
 <span data-ttu-id="8ef67-106">[out] Un pointeur d’interface de type [ICLRControl, Interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md) qui permet aux hôtes de configurer des aspects supplémentaires du CLR.</span><span class="sxs-lookup"><span data-stu-id="8ef67-106">[out] An interface pointer of type [ICLRControl Interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md) that enables hosts to configure additional aspects of the CLR.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8ef67-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8ef67-107">Return Value</span></span>  
  
|<span data-ttu-id="8ef67-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8ef67-108">HRESULT</span></span>|<span data-ttu-id="8ef67-109">Description</span><span class="sxs-lookup"><span data-stu-id="8ef67-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8ef67-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ef67-110">S_OK</span></span>|<span data-ttu-id="8ef67-111">`GetCLRControl` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="8ef67-111">`GetCLRControl` returned successfully.</span></span>|  
|<span data-ttu-id="8ef67-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8ef67-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8ef67-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="8ef67-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8ef67-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8ef67-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8ef67-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="8ef67-115">The call timed out.</span></span>|  
|<span data-ttu-id="8ef67-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8ef67-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8ef67-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="8ef67-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8ef67-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8ef67-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8ef67-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="8ef67-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8ef67-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8ef67-120">E_FAIL</span></span>|<span data-ttu-id="8ef67-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8ef67-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8ef67-122">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="8ef67-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8ef67-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="8ef67-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="8ef67-124">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="8ef67-124">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="8ef67-125">Le CLR a déjà démarré.</span><span class="sxs-lookup"><span data-stu-id="8ef67-125">The CLR has already started.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8ef67-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8ef67-126">Remarks</span></span>  
 <span data-ttu-id="8ef67-127">`ICLRControl` fournit le [GetCLRManager, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) (méthode), ce qui permet à l’hôte obtenir un pointeur d’interface à un des types de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="8ef67-127">`ICLRControl` provides the [GetCLRManager Method](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method, which enables the host to get an interface pointer to one of the manager types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ef67-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ef67-128">Requirements</span></span>  
 <span data-ttu-id="8ef67-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ef67-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ef67-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8ef67-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8ef67-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8ef67-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8ef67-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ef67-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ef67-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ef67-133">See also</span></span>
- [<span data-ttu-id="8ef67-134">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="8ef67-134">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="8ef67-135">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="8ef67-135">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
