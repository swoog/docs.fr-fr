---
title: ICLRRuntimeHost::GetCurrentAppDomainId, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.GetCurrentAppDomainId
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::GetCurrentAppDomainId
helpviewer_keywords:
- ICLRRuntimeHost::GetCurrentAppDomainId method [.NET Framework hosting]
- GetCurrentAppDomainId method [.NET Framework hosting]
ms.assetid: 33800475-7815-4976-8aca-a1038761a2ef
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 192492c232970842270f031832d1eb46357ec07f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527170"
---
# <a name="iclrruntimehostgetcurrentappdomainid-method"></a><span data-ttu-id="e8e42-102">ICLRRuntimeHost::GetCurrentAppDomainId, méthode</span><span class="sxs-lookup"><span data-stu-id="e8e42-102">ICLRRuntimeHost::GetCurrentAppDomainId Method</span></span>
<span data-ttu-id="e8e42-103">Obtient l’identificateur numérique de la <xref:System.AppDomain> qui est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e8e42-103">Gets the numeric identifier of the <xref:System.AppDomain> that is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8e42-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8e42-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentAppDomainId(  
    [out] DWORD* pdwAppDomainId  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8e42-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8e42-105">Parameters</span></span>  
 `pdwAppDomainId`  
 <span data-ttu-id="e8e42-106">[out] L’identificateur numérique de la <xref:System.AppDomain> qui est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e8e42-106">[out] The numeric identifier of the <xref:System.AppDomain> that is currently executing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e8e42-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e8e42-107">Return Value</span></span>  
  
|<span data-ttu-id="e8e42-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e8e42-108">HRESULT</span></span>|<span data-ttu-id="e8e42-109">Description</span><span class="sxs-lookup"><span data-stu-id="e8e42-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e8e42-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8e42-110">S_OK</span></span>|<span data-ttu-id="e8e42-111">`GetCurrentAppDomainId` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="e8e42-111">`GetCurrentAppDomainId` returned successfully.</span></span>|  
|<span data-ttu-id="e8e42-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e8e42-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e8e42-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="e8e42-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e8e42-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e8e42-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e8e42-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="e8e42-115">The call timed out.</span></span>|  
|<span data-ttu-id="e8e42-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e8e42-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e8e42-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="e8e42-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e8e42-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e8e42-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e8e42-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="e8e42-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e8e42-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e8e42-120">E_FAIL</span></span>|<span data-ttu-id="e8e42-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e8e42-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e8e42-122">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="e8e42-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e8e42-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e8e42-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e8e42-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e8e42-124">Remarks</span></span>  
 <span data-ttu-id="e8e42-125">Le `pdwAppDomainId` paramètre est défini sur la valeur de la <xref:System.AppDomain.Id%2A> propriété de la <xref:System.AppDomain> dans lequel s’exécute le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="e8e42-125">The `pdwAppDomainId` parameter is set to the value of the <xref:System.AppDomain.Id%2A> property of the <xref:System.AppDomain> in which the current thread is executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8e42-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e8e42-126">Requirements</span></span>  
 <span data-ttu-id="e8e42-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8e42-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8e42-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e8e42-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e8e42-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e8e42-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e8e42-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8e42-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8e42-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8e42-131">See also</span></span>
- <xref:System.AppDomain>
- <xref:System.AppDomainManager>
- [<span data-ttu-id="e8e42-132">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="e8e42-132">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
