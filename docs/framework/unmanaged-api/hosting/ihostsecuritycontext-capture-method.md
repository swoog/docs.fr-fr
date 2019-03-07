---
title: IHostSecurityContext::Capture, méthode
ms.date: 03/30/2017
api_name:
- IHostSecurityContext.Capture
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityContext::Capture
helpviewer_keywords:
- Capture method [.NET Framework hosting]
- IHostSecurityContext::Capture method [.NET Framework hosting]
ms.assetid: ae0836d0-1170-4494-bac5-d0e809df51a2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 92b593248a7a196247a5b4c71a90cd8944665bbe
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57485276"
---
# <a name="ihostsecuritycontextcapture-method"></a><span data-ttu-id="fd9c9-102">IHostSecurityContext::Capture, méthode</span><span class="sxs-lookup"><span data-stu-id="fd9c9-102">IHostSecurityContext::Capture Method</span></span>
<span data-ttu-id="fd9c9-103">Obtient un clone de le [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) instance retournée à partir d’un appel à [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md).</span><span class="sxs-lookup"><span data-stu-id="fd9c9-103">Gets a clone of the [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) instance returned from a call to [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd9c9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd9c9-104">Syntax</span></span>  
  
```  
HRESULT Capture (  
    [out] IHostSecurityContext** ppClonedContext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd9c9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd9c9-105">Parameters</span></span>  
 `ppClonedContext`  
 <span data-ttu-id="fd9c9-106">[out] Un pointeur vers l’adresse d’un clone de le `IHostSecurityContext` objet devant être capturés.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-106">[out] A pointer to the address of a clone of the `IHostSecurityContext` object to be captured.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fd9c9-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fd9c9-107">Return Value</span></span>  
  
|<span data-ttu-id="fd9c9-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fd9c9-108">HRESULT</span></span>|<span data-ttu-id="fd9c9-109">Description</span><span class="sxs-lookup"><span data-stu-id="fd9c9-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fd9c9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd9c9-110">S_OK</span></span>|<span data-ttu-id="fd9c9-111">`Capture` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-111">`Capture` returned successfully.</span></span>|  
|<span data-ttu-id="fd9c9-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fd9c9-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fd9c9-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="fd9c9-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fd9c9-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="fd9c9-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-115">The call timed out.</span></span>|  
|<span data-ttu-id="fd9c9-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="fd9c9-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="fd9c9-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="fd9c9-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="fd9c9-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="fd9c9-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="fd9c9-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fd9c9-120">E_FAIL</span></span>|<span data-ttu-id="fd9c9-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="fd9c9-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="fd9c9-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fd9c9-124">Notes</span><span class="sxs-lookup"><span data-stu-id="fd9c9-124">Remarks</span></span>  
 <span data-ttu-id="fd9c9-125">Le pointeur d’interface retourné par `Capture` est un clone du contexte capturé.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-125">The interface pointer returned from `Capture` is a clone of the captured context.</span></span> <span data-ttu-id="fd9c9-126">Lorsque ces informations sont déplacées sur un point de code asynchrone, sa durée de vie est séparée de celui du pointeur par rapport à laquelle l’appel a été effectué.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-126">When this information is moved across an asynchronous code point, its lifetime is separated from that of the pointer against which the call was made.</span></span> <span data-ttu-id="fd9c9-127">Le pointeur d’origine peut par conséquent être libéré.</span><span class="sxs-lookup"><span data-stu-id="fd9c9-127">The original pointer can therefore be released.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd9c9-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd9c9-128">Requirements</span></span>  
 <span data-ttu-id="fd9c9-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fd9c9-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd9c9-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fd9c9-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fd9c9-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fd9c9-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fd9c9-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd9c9-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd9c9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd9c9-133">See also</span></span>
- [<span data-ttu-id="fd9c9-134">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="fd9c9-134">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)
- [<span data-ttu-id="fd9c9-135">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="fd9c9-135">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)
