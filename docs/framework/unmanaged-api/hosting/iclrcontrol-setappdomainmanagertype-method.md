---
title: ICLRControl::SetAppDomainManagerType, méthode
ms.date: 03/30/2017
api_name:
- ICLRControl.SetAppDomainManagerType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl::SetAppDomainManagerType
helpviewer_keywords:
- SetAppDomainManagerType method, ICLRControl interface [.NET Framework hosting]
- ICLRControl::SetAppDomainManagerType method [.NET Framework hosting]
ms.assetid: ec57828b-2aad-496d-a35a-e45d4bd7fe77
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: be778fed910b2cbdbf5e9ae7754abae437ef6bec
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433732"
---
# <a name="iclrcontrolsetappdomainmanagertype-method"></a><span data-ttu-id="e3256-102">ICLRControl::SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="e3256-102">ICLRControl::SetAppDomainManagerType Method</span></span>
<span data-ttu-id="e3256-103">Définit un type dérivé <xref:System.AppDomainManager> comme type pour les gestionnaires de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="e3256-103">Sets a type derived from <xref:System.AppDomainManager> as the type for application domain managers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3256-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3256-104">Syntax</span></span>  
  
```  
HRESULT SetAppDomainManagerType (  
    [in] LPCWSTR pwzAppDomainManagerAssembly,  
    [in] LPCWSTR pwzAppDomainManagerType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e3256-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3256-105">Parameters</span></span>  
 `pwzAppDomainManagerAssembly`  
 <span data-ttu-id="e3256-106">[in] Le nom de l’assembly dans lequel le type demandé dérivé <xref:System.AppDomainManager> est implémentée.</span><span class="sxs-lookup"><span data-stu-id="e3256-106">[in] The name of the assembly in which the requested type derived from <xref:System.AppDomainManager> is implemented.</span></span>  
  
 `pwzAppDomainManagerType`  
 <span data-ttu-id="e3256-107">[in] Le nom du type implémenté dans le `pwzAppDomainManagerAssembly` paramètre qui implémente les fonctionnalités de <xref:System.AppDomainManager>.</span><span class="sxs-lookup"><span data-stu-id="e3256-107">[in] The name of the type implemented in the `pwzAppDomainManagerAssembly` parameter that implements the capabilities of <xref:System.AppDomainManager>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e3256-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e3256-108">Return Value</span></span>  
  
|<span data-ttu-id="e3256-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e3256-109">HRESULT</span></span>|<span data-ttu-id="e3256-110">Description</span><span class="sxs-lookup"><span data-stu-id="e3256-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e3256-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3256-111">S_OK</span></span>|<span data-ttu-id="e3256-112">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="e3256-112">The method returned successfully.</span></span>|  
|<span data-ttu-id="e3256-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e3256-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e3256-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="e3256-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e3256-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e3256-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e3256-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="e3256-116">The call timed out.</span></span>|  
|<span data-ttu-id="e3256-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e3256-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e3256-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="e3256-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e3256-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e3256-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e3256-120">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="e3256-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e3256-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e3256-121">E_FAIL</span></span>|<span data-ttu-id="e3256-122">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e3256-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e3256-123">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="e3256-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e3256-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e3256-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e3256-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3256-125">Requirements</span></span>  
 <span data-ttu-id="e3256-126">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e3256-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3256-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e3256-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e3256-128">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e3256-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e3256-129">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3256-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3256-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3256-130">See Also</span></span>  
 [<span data-ttu-id="e3256-131">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="e3256-131">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="e3256-132">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="e3256-132">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
