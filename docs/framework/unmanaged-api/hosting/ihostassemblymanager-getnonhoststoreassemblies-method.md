---
title: IHostAssemblyManager::GetNonHostStoreAssemblies, méthode
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager.GetNonHostStoreAssemblies
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager::GetNonHostStoreAssemblies
helpviewer_keywords:
- IHostAssemblyManager::GetNonHostStoreAssemblies method [.NET Framework hosting]
- GetNonHostStoreAssemblies method [.NET Framework hosting]
ms.assetid: d2250b38-c76a-40ce-80c8-ba45149886e8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b0da548d5d5cc22eb6754859a802afa4d82fac89
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438387"
---
# <a name="ihostassemblymanagergetnonhoststoreassemblies-method"></a><span data-ttu-id="f8fd5-102">IHostAssemblyManager::GetNonHostStoreAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="f8fd5-102">IHostAssemblyManager::GetNonHostStoreAssemblies Method</span></span>
<span data-ttu-id="f8fd5-103">Obtient un pointeur d’interface vers un [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) qui représente la liste des assemblys qui l’hôte attend que le common language runtime (CLR) à charger.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-103">Gets an interface pointer to an [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) that represents the list of assemblies that the host expects the common language runtime (CLR) to load.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8fd5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8fd5-104">Syntax</span></span>  
  
```  
HRESULT GetNonHostStoreAssemblies (  
    [out] ICLRAssemblyReferenceList **ppReferenceList  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f8fd5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8fd5-105">Parameters</span></span>  
 `ppReferenceList`  
 <span data-ttu-id="f8fd5-106">[out] Un pointeur vers l’adresse d’un `ICLRAssemblyReferenceList` qui contient une liste de références aux assemblys qui l’hôte attend que le CLR à charger.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-106">[out] A pointer to the address of an `ICLRAssemblyReferenceList` that contains a list of references to assemblies that the host expects the CLR to load.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f8fd5-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f8fd5-107">Return Value</span></span>  
  
|<span data-ttu-id="f8fd5-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f8fd5-108">HRESULT</span></span>|<span data-ttu-id="f8fd5-109">Description</span><span class="sxs-lookup"><span data-stu-id="f8fd5-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f8fd5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8fd5-110">S_OK</span></span>|<span data-ttu-id="f8fd5-111">`GetNonHostStoreAssemblies` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-111">`GetNonHostStoreAssemblies` returned successfully.</span></span>|  
|<span data-ttu-id="f8fd5-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f8fd5-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f8fd5-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f8fd5-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f8fd5-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f8fd5-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-115">The call timed out.</span></span>|  
|<span data-ttu-id="f8fd5-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f8fd5-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f8fd5-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f8fd5-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f8fd5-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f8fd5-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f8fd5-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f8fd5-120">E_FAIL</span></span>|<span data-ttu-id="f8fd5-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f8fd5-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f8fd5-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f8fd5-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f8fd5-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="f8fd5-125">Pas assez de mémoire n’était disponible pour créer la liste de références pour demandé `ICLRAssemblyReferenceList`.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-125">Not enough memory was available to create the list of references for the requested `ICLRAssemblyReferenceList`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f8fd5-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f8fd5-126">Remarks</span></span>  
 <span data-ttu-id="f8fd5-127">Le CLR résout les références à l’aide de l’ensemble des recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8fd5-127">The CLR resolves references using the following set of guidelines:</span></span>  
  
-   <span data-ttu-id="f8fd5-128">Tout d’abord, il consulte la liste des références d’assembly retourné par `GetNonHostStoreAssemblies`.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-128">First, it consults the list of assembly references returned by `GetNonHostStoreAssemblies`.</span></span>  
  
-   <span data-ttu-id="f8fd5-129">Si l’assembly s’affiche dans la liste, le CLR se lie normalement à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-129">If the assembly appears in the list, the CLR binds to it normally.</span></span>  
  
-   <span data-ttu-id="f8fd5-130">Si l’assembly n’apparaît pas dans la liste et que l’hôte a fourni une implémentation de [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md), le CLR appelle [IHostAssemblyStore::ProvideAssembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) pour autoriser l’hôte de fournir le assembly à lier.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-130">If the assembly does not appear in the list and the host has provided an implementation of [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md), the CLR calls [IHostAssemblyStore::ProvideAssembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) to allow the host to supply the assembly to bind to.</span></span>  
  
-   <span data-ttu-id="f8fd5-131">Sinon, le CLR ne peut pas lier à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-131">Otherwise, the CLR fails to bind to the assembly.</span></span>  
  
 <span data-ttu-id="f8fd5-132">Si l’hôte définit `ppReferenceList` à null, les sondes premier CLR appelle le global assembly cache, `ProvideAssembly`et tente ensuite de détecter la base de l’application pour résoudre une référence d’assembly.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-132">If the host sets `ppReferenceList` to null, the CLR first probes the global assembly cache, calls `ProvideAssembly`, and then probes the application base to resolve an assembly reference.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f8fd5-133">Lors de l’initialisation, le CLR appelle `GetNonHostStoreAssemblies` qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-133">Upon initialization, the CLR calls `GetNonHostStoreAssemblies` only once.</span></span> <span data-ttu-id="f8fd5-134">La méthode n’est pas appelée à nouveau.</span><span class="sxs-lookup"><span data-stu-id="f8fd5-134">The method is not called again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8fd5-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8fd5-135">Requirements</span></span>  
 <span data-ttu-id="f8fd5-136">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f8fd5-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8fd5-137">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f8fd5-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f8fd5-138">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f8fd5-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f8fd5-139">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8fd5-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8fd5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8fd5-140">See Also</span></span>  
 [<span data-ttu-id="f8fd5-141">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="f8fd5-141">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [<span data-ttu-id="f8fd5-142">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="f8fd5-142">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="f8fd5-143">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="f8fd5-143">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
