---
title: ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream, méthode
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetReferencedAssembliesFromStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream
helpviewer_keywords:
- ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream method [.NET Framework hosting]
- GetReferencedAssembliesFromStream method [.NET Framework hosting]
ms.assetid: fe9849c1-c3fc-477b-a31f-e8619f5516f5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 49fc3cf6aff94b5914040fba77acd0769fc73a43
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57490032"
---
# <a name="iclrassemblyidentitymanagergetreferencedassembliesfromstream-method"></a><span data-ttu-id="fa6bb-102">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream, méthode</span><span class="sxs-lookup"><span data-stu-id="fa6bb-102">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream Method</span></span>
<span data-ttu-id="fa6bb-103">Obtient un pointeur vers un [ICLRReferenceAssemblyEnum](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md) objet qui contient les données d’identité pour les assemblys référencés par l’assembly dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-103">Gets a pointer to an [ICLRReferenceAssemblyEnum](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md) object that contains assembly identity data for the assemblies referenced by the assembly in the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa6bb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa6bb-104">Syntax</span></span>  
  
```  
HRESULT GetReferencedAssembliesFromStream (  
    [in]  IStream *pStream,  
    [in]  DWORD    dwFlags,  
    [in]  ICLRAssemblyReferenceList  *pExcludeAssembliesList,  
    [out] ICLRReferenceAssemblyEnum **ppReferenceEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa6bb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa6bb-105">Parameters</span></span>  
 `pStream`  
 <span data-ttu-id="fa6bb-106">[in] Un pointeur d’interface vers un `IStream` contenant l’assembly doit être évaluée.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-106">[in] An interface pointer to an `IStream` containing the assembly to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="fa6bb-107">[in] Fourni pour des extensibilités futures.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-107">[in] Provided for future extensibility.</span></span> <span data-ttu-id="fa6bb-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT est la seule valeur de la version actuelle du common language runtime (CLR) prend en charge.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-108">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pExcludeAssembliesList`  
 <span data-ttu-id="fa6bb-109">[in] Un pointeur vers un [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) objet qui contient les données d’identité pour les assemblys à exclure de `ppReferenceEnum`.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-109">[in] A pointer to an [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) object that contains assembly identity data for the assemblies to be excluded from `ppReferenceEnum`.</span></span>  
  
 `ppReferenceEnum`  
 <span data-ttu-id="fa6bb-110">[out] Un pointeur vers l’adresse d’un `ICLRReferenceAssemblyEnum` objet qui contient les données d’identité pour les assemblys référencés par l’assembly dans `pStream`, à l’exclusion des assemblys dans `pExcludeAssembliesList`.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-110">[out] A pointer to the address of an `ICLRReferenceAssemblyEnum` object that contains assembly identity data for the assemblies referenced by the assembly in `pStream`, excluding the assemblies in `pExcludeAssembliesList`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fa6bb-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fa6bb-111">Return Value</span></span>  
  
|<span data-ttu-id="fa6bb-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fa6bb-112">HRESULT</span></span>|<span data-ttu-id="fa6bb-113">Description</span><span class="sxs-lookup"><span data-stu-id="fa6bb-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fa6bb-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa6bb-114">S_OK</span></span>|<span data-ttu-id="fa6bb-115">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-115">The method returned successfully.</span></span>|  
|<span data-ttu-id="fa6bb-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fa6bb-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fa6bb-117">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="fa6bb-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fa6bb-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="fa6bb-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-119">The call timed out.</span></span>|  
|<span data-ttu-id="fa6bb-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="fa6bb-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="fa6bb-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="fa6bb-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="fa6bb-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="fa6bb-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="fa6bb-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fa6bb-124">E_FAIL</span></span>|<span data-ttu-id="fa6bb-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="fa6bb-126">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-126">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="fa6bb-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fa6bb-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fa6bb-128">Remarks</span></span>  
 <span data-ttu-id="fa6bb-129">L’appelant peut choisir d’exclure un ensemble de références d’assembly connus dans la liste renvoyée.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-129">The caller can choose to exclude a set of known assembly references from the returned list.</span></span> <span data-ttu-id="fa6bb-130">Cet ensemble est défini par `pExcludeAssembliesList`.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-130">This set is defined by `pExcludeAssembliesList`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa6bb-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa6bb-131">Requirements</span></span>  
 <span data-ttu-id="fa6bb-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa6bb-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa6bb-133">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fa6bb-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fa6bb-134">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fa6bb-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fa6bb-135">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa6bb-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa6bb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa6bb-136">See also</span></span>
- [<span data-ttu-id="fa6bb-137">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="fa6bb-137">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="fa6bb-138">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="fa6bb-138">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="fa6bb-139">ICLRReferenceAssemblyEnum, interface</span><span class="sxs-lookup"><span data-stu-id="fa6bb-139">ICLRReferenceAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md)
