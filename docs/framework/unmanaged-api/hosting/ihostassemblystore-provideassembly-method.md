---
title: IHostAssemblyStore::ProvideAssembly, méthode
ms.date: 03/30/2017
api_name:
- IHostAssemblyStore.ProvideAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyStore::ProvideAssembly
helpviewer_keywords:
- ProvideAssembly method [.NET Framework hosting]
- IHostAssemblyStore::ProvideAssembly method [.NET Framework hosting]
ms.assetid: 625c3dd5-a3f0-442c-adde-310dadbb5054
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 62a8be1e330338043df50bd80576b5aa65447b9c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59111902"
---
# <a name="ihostassemblystoreprovideassembly-method"></a><span data-ttu-id="7dab9-102">IHostAssemblyStore::ProvideAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="7dab9-102">IHostAssemblyStore::ProvideAssembly Method</span></span>
<span data-ttu-id="7dab9-103">Obtient une référence à un assembly qui n’est pas référencé par le [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) qui est retourné à partir de [IHostAssemblyManager::GetNonHostStoreAssemblies](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md).</span><span class="sxs-lookup"><span data-stu-id="7dab9-103">Gets a reference to an assembly that is not referenced by the [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) that is returned from [IHostAssemblyManager::GetNonHostStoreAssemblies](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md).</span></span> <span data-ttu-id="7dab9-104">Le common language runtime (CLR) appelle `ProvideAssembly` pour chaque assembly qui n’apparaît pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7dab9-104">The common language runtime (CLR) calls `ProvideAssembly` for each assembly that does not appear in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7dab9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dab9-105">Syntax</span></span>  
  
```  
HRESULT ProvideAssembly (  
    [in]  AssemblyBindInfo *pBindInfo,  
    [out] UINT64           *pAssemblyId,  
    [out] UINT64           *pHostContext,  
    [out] IStream          **ppStmAssemblyImage,  
    [out] IStream          **ppStmPDB  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7dab9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dab9-106">Parameters</span></span>  
 `pBindInfo`  
 <span data-ttu-id="7dab9-107">[in] Un pointeur vers un [AssemblyBindInfo](../../../../docs/framework/unmanaged-api/hosting/assemblybindinfo-structure.md) instance que l’hôte utilise pour déterminer certaines caractéristiques de liaison, y compris la présence ou l’absence de toute stratégie de contrôle de version et l’assembly à lier.</span><span class="sxs-lookup"><span data-stu-id="7dab9-107">[in] A pointer to an [AssemblyBindInfo](../../../../docs/framework/unmanaged-api/hosting/assemblybindinfo-structure.md) instance that the host uses to determine certain bind characteristics, including the presence or absence of any versioning policy, and which assembly to bind to.</span></span>  
  
 `pAssemblyId`  
 <span data-ttu-id="7dab9-108">[out] Un pointeur vers un identificateur unique pour l’assembly demandé pour ce `IStream`.</span><span class="sxs-lookup"><span data-stu-id="7dab9-108">[out] A pointer to a unique identifier for the requested assembly for this `IStream`.</span></span>  
  
 `pHostContext`  
 <span data-ttu-id="7dab9-109">[out] Un pointeur vers les données spécifiques à l’hôte qui sont utilisés pour déterminer la preuve de l’assembly demandé sans avoir besoin d’une plateforme de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7dab9-109">[out] A pointer to host-specific data that is used to determine the evidence of the requested assembly without the need of a platform invoke call.</span></span> `pHostContext` <span data-ttu-id="7dab9-110">correspond à la <xref:System.Reflection.Assembly.HostContext%2A> propriété de managé <xref:System.Reflection.Assembly> classe.</span><span class="sxs-lookup"><span data-stu-id="7dab9-110">corresponds to the <xref:System.Reflection.Assembly.HostContext%2A> property of the managed <xref:System.Reflection.Assembly> class.</span></span>  
  
 `ppStmAssemblyImage`  
 <span data-ttu-id="7dab9-111">[out] Un pointeur vers l’adresse d’un `IStream` qui contient l’image exécutable portable (PE) à charger, ou null si l’assembly est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7dab9-111">[out] A pointer to the address of an `IStream` that contains the portable executable (PE) image to be loaded, or null if the assembly could not be found.</span></span>  
  
 `ppStmPDB`  
 <span data-ttu-id="7dab9-112">[out] Un pointeur vers l’adresse d’un `IStream` qui contient les informations de débogage (PDB) de programme, ou null si le fichier .pdb est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7dab9-112">[out] A pointer to the address of an `IStream` that contains the program debug (PDB) information, or null if the .pdb file could not be found.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7dab9-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7dab9-113">Return Value</span></span>  
  
|<span data-ttu-id="7dab9-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7dab9-114">HRESULT</span></span>|<span data-ttu-id="7dab9-115">Description</span><span class="sxs-lookup"><span data-stu-id="7dab9-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7dab9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7dab9-116">S_OK</span></span>|`ProvideAssembly` <span data-ttu-id="7dab9-117">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="7dab9-117">returned successfully.</span></span>|  
|<span data-ttu-id="7dab9-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7dab9-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7dab9-119">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="7dab9-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7dab9-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7dab9-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7dab9-121">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="7dab9-121">The call timed out.</span></span>|  
|<span data-ttu-id="7dab9-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7dab9-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7dab9-123">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="7dab9-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7dab9-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7dab9-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7dab9-125">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="7dab9-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7dab9-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7dab9-126">E_FAIL</span></span>|<span data-ttu-id="7dab9-127">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7dab9-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7dab9-128">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="7dab9-128">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7dab9-129">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="7dab9-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="7dab9-130">COR_E_FILENOTFOUND (0x80070002)</span><span class="sxs-lookup"><span data-stu-id="7dab9-130">COR_E_FILENOTFOUND (0x80070002)</span></span>|<span data-ttu-id="7dab9-131">L’assembly demandé n’a pas pu être localisé.</span><span class="sxs-lookup"><span data-stu-id="7dab9-131">The requested assembly could not be located.</span></span>|  
|<span data-ttu-id="7dab9-132">E_NOT_SUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="7dab9-132">E_NOT_SUFFICIENT_BUFFER</span></span>|<span data-ttu-id="7dab9-133">La taille de mémoire tampon spécifiée par `pAssemblyId` n’est pas suffisamment grande pour contenir l’identificateur que l’hôte souhaite retourner.</span><span class="sxs-lookup"><span data-stu-id="7dab9-133">The buffer size specified by `pAssemblyId` is not large enough to hold the identifier that the host wants to return.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7dab9-134">Notes</span><span class="sxs-lookup"><span data-stu-id="7dab9-134">Remarks</span></span>  
 <span data-ttu-id="7dab9-135">La valeur d’identité retournée pour `pAssemblyId` est spécifié par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7dab9-135">The identity value returned for `pAssemblyId` is specified by the host.</span></span> <span data-ttu-id="7dab9-136">Les identificateurs doivent être uniques au sein de la durée de vie d’un processus.</span><span class="sxs-lookup"><span data-stu-id="7dab9-136">Identifiers must be unique within the lifetime of a process.</span></span> <span data-ttu-id="7dab9-137">Le CLR utilise cette valeur comme identificateur unique pour le flux.</span><span class="sxs-lookup"><span data-stu-id="7dab9-137">The CLR uses this value as a unique identifier for the stream.</span></span> <span data-ttu-id="7dab9-138">Il vérifie chaque valeur sur les valeurs de `pAssemblyId` retourné par d’autres appels à `ProvideAssembly`.</span><span class="sxs-lookup"><span data-stu-id="7dab9-138">It checks each value against the values for `pAssemblyId` returned by other calls to `ProvideAssembly`.</span></span> <span data-ttu-id="7dab9-139">Si l’hôte renvoie le même type `pAssemblyId` valeur pour un autre `IStream`, le CLR vérifie si le contenu de ce flux a déjà été mappé.</span><span class="sxs-lookup"><span data-stu-id="7dab9-139">If the host returns the same `pAssemblyId` value for another `IStream`, the CLR checks whether the contents of that stream have already been mapped.</span></span> <span data-ttu-id="7dab9-140">Dans ce cas, le runtime charge la copie existante de l’image au lieu de mapper une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="7dab9-140">If so, the runtime loads the existing copy of the image instead of mapping a new one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7dab9-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dab9-141">Requirements</span></span>  
 <span data-ttu-id="7dab9-142">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7dab9-142">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7dab9-143">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="7dab9-143">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7dab9-144">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7dab9-144">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="7dab9-145">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7dab9-145">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7dab9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dab9-146">See also</span></span>

- [<span data-ttu-id="7dab9-147">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="7dab9-147">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="7dab9-148">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="7dab9-148">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [<span data-ttu-id="7dab9-149">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="7dab9-149">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
