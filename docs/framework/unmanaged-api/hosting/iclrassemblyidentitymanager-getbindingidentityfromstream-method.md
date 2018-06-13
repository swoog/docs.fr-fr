---
title: ICLRAssemblyIdentityManager::GetBindingIdentityFromStream, méthode
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetBindingIdentityFromStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetBindingIdentityFromStream
helpviewer_keywords:
- GetBindingIdentityFromStream method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::GetBindingIdentityFromStream method [.NET Framework hosting]
ms.assetid: 40123b30-a589-46b3-95d3-af7b2b0baa05
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 57cf4e9f79be8e705869cf986a586fcfb3359584
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435337"
---
# <a name="iclrassemblyidentitymanagergetbindingidentityfromstream-method"></a><span data-ttu-id="3626f-102">ICLRAssemblyIdentityManager::GetBindingIdentityFromStream, méthode</span><span class="sxs-lookup"><span data-stu-id="3626f-102">ICLRAssemblyIdentityManager::GetBindingIdentityFromStream Method</span></span>
<span data-ttu-id="3626f-103">Obtient les données d’identité canonique de l’assembly dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="3626f-103">Gets the canonical assembly identity data for the assembly in the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3626f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3626f-104">Syntax</span></span>  
  
```  
HRESULT GetBindingIdentityFromStream (  
    [in] IStream    *pStream,  
    [in] DWORD       dwFlags,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3626f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3626f-105">Parameters</span></span>  
 `pStream`  
 <span data-ttu-id="3626f-106">[in] Le flux d’assembly à évaluer.</span><span class="sxs-lookup"><span data-stu-id="3626f-106">[in] The assembly stream to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="3626f-107">[in] Fourni pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="3626f-107">[in] Provided for future extensibility.</span></span> <span data-ttu-id="3626f-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT est la seule valeur de la version actuelle du common language runtime (CLR) prend en charge.</span><span class="sxs-lookup"><span data-stu-id="3626f-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="3626f-109">[out] Une mémoire tampon qui contient les données d’identité assembly opaque.</span><span class="sxs-lookup"><span data-stu-id="3626f-109">[out] A buffer containing the opaque assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="3626f-110">[dans, out] La taille de `pwzBuffer`.</span><span class="sxs-lookup"><span data-stu-id="3626f-110">[in, out] The size of `pwzBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3626f-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3626f-111">Return Value</span></span>  
  
|<span data-ttu-id="3626f-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3626f-112">HRESULT</span></span>|<span data-ttu-id="3626f-113">Description</span><span class="sxs-lookup"><span data-stu-id="3626f-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3626f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3626f-114">S_OK</span></span>|<span data-ttu-id="3626f-115">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3626f-115">The method returned successfully.</span></span>|  
|<span data-ttu-id="3626f-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3626f-116">E_INVALIDARG</span></span>|<span data-ttu-id="3626f-117">Fourni `pStream` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3626f-117">The supplied `pStream` is null.</span></span>|  
|<span data-ttu-id="3626f-118">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="3626f-118">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="3626f-119">La taille de `pwzBuffer` est trop petite.</span><span class="sxs-lookup"><span data-stu-id="3626f-119">The size of `pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="3626f-120">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3626f-120">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3626f-121">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="3626f-121">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3626f-122">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3626f-122">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3626f-123">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="3626f-123">The call timed out.</span></span>|  
|<span data-ttu-id="3626f-124">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3626f-124">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3626f-125">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="3626f-125">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3626f-126">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3626f-126">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3626f-127">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="3626f-127">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3626f-128">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3626f-128">E_FAIL</span></span>|<span data-ttu-id="3626f-129">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3626f-129">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3626f-130">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="3626f-130">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3626f-131">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="3626f-131">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3626f-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3626f-132">Requirements</span></span>  
 <span data-ttu-id="3626f-133">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3626f-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3626f-134">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3626f-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3626f-135">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3626f-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3626f-136">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3626f-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3626f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3626f-137">See Also</span></span>  
 [<span data-ttu-id="3626f-138">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="3626f-138">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)  
 [<span data-ttu-id="3626f-139">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="3626f-139">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
