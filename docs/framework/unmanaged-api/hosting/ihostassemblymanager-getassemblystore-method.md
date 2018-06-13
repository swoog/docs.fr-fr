---
title: IHostAssemblyManager::GetAssemblyStore, méthode
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager.GetAssemblyStore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager::GetAssemblyStore
helpviewer_keywords:
- IHostAssemblyManager::GetAssemblyStore method [.NET Framework hosting]
- GetAssemblyStore method [.NET Framework hosting]
ms.assetid: d0f74593-9bb1-4a11-8096-e29734b20698
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: efad3c6e566ab35a8ba4fbbacf09931e844ce8ef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438349"
---
# <a name="ihostassemblymanagergetassemblystore-method"></a><span data-ttu-id="3b673-102">IHostAssemblyManager::GetAssemblyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="3b673-102">IHostAssemblyManager::GetAssemblyStore Method</span></span>
<span data-ttu-id="3b673-103">Obtient un pointeur d’interface vers un [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) qui représente la liste des assemblys chargés par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="3b673-103">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b673-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b673-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyStore (  
    [out] IHostAssemblyStore **ppAssemblyStore  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3b673-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b673-105">Parameters</span></span>  
 `ppAssemblyStore`  
 <span data-ttu-id="3b673-106">[out] Un pointeur de fonction vers un `IHostAssemblyStore` de l’instance, ou null si l’hôte n’implémente pas `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="3b673-106">[out] A function pointer to an `IHostAssemblyStore` instance, or null, if the host does not implement `IHostAssemblyStore`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3b673-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3b673-107">Return Value</span></span>  
  
|<span data-ttu-id="3b673-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3b673-108">HRESULT</span></span>|<span data-ttu-id="3b673-109">Description</span><span class="sxs-lookup"><span data-stu-id="3b673-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3b673-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b673-110">S_OK</span></span>|<span data-ttu-id="3b673-111">`GetAssemblyStore` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3b673-111">`GetAssemblyStore` returned successfully.</span></span>|  
|<span data-ttu-id="3b673-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3b673-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3b673-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="3b673-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3b673-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3b673-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3b673-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="3b673-115">The call timed out.</span></span>|  
|<span data-ttu-id="3b673-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3b673-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3b673-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="3b673-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3b673-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3b673-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3b673-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="3b673-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3b673-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3b673-120">E_FAIL</span></span>|<span data-ttu-id="3b673-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3b673-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3b673-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="3b673-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3b673-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="3b673-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="3b673-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="3b673-124">E_NOINTERFACE</span></span>|<span data-ttu-id="3b673-125">L’hôte ne fournit pas une implémentation de `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="3b673-125">The host does not provide an implementation of `IHostAssemblyStore`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3b673-126">Notes</span><span class="sxs-lookup"><span data-stu-id="3b673-126">Remarks</span></span>  
 <span data-ttu-id="3b673-127">`IHostAssemblyStore` Fournit des méthodes qui permettent à un hôte à lier à des assemblys et des modules indépendamment du CLR.</span><span class="sxs-lookup"><span data-stu-id="3b673-127">`IHostAssemblyStore` provides methods that allow a host to bind to assemblies and modules independently of the CLR.</span></span> <span data-ttu-id="3b673-128">Hôtes fournissent généralement des magasins pour autoriser les assemblys à charger à partir d’autres formats que le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3b673-128">Hosts typically provide assembly stores to allow assemblies to be loaded from formats other than the file system.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3b673-129">Si l’hôte n’implémente pas `IHostAssemblyStore`, `GetAssemblyStore` doit retourner une valeur HRESULT d’E_NOINTERFACE et doit définir `ppAssemblyStore` avec la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3b673-129">If the host does not implement `IHostAssemblyStore`, `GetAssemblyStore` should return an HRESULT value of E_NOINTERFACE, and should set `ppAssemblyStore` to null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b673-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b673-130">Requirements</span></span>  
 <span data-ttu-id="3b673-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b673-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b673-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3b673-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3b673-133">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3b673-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3b673-134">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b673-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b673-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b673-135">See Also</span></span>  
 [<span data-ttu-id="3b673-136">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="3b673-136">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="3b673-137">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="3b673-137">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
