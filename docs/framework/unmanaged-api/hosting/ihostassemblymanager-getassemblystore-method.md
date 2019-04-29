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
ms.openlocfilehash: 35e38949ce945d93216daffd3c0d91dad6c8739b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763189"
---
# <a name="ihostassemblymanagergetassemblystore-method"></a><span data-ttu-id="878d3-102">IHostAssemblyManager::GetAssemblyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="878d3-102">IHostAssemblyManager::GetAssemblyStore Method</span></span>
<span data-ttu-id="878d3-103">Obtient un pointeur d’interface vers un [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) qui représente la liste des assemblys chargés par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="878d3-103">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="878d3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="878d3-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyStore (  
    [out] IHostAssemblyStore **ppAssemblyStore  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="878d3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="878d3-105">Parameters</span></span>  
 `ppAssemblyStore`  
 <span data-ttu-id="878d3-106">[out] Un pointeur de fonction vers une `IHostAssemblyStore` de l’instance, ou null si l’hôte n’implémente pas `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="878d3-106">[out] A function pointer to an `IHostAssemblyStore` instance, or null, if the host does not implement `IHostAssemblyStore`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="878d3-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="878d3-107">Return Value</span></span>  
  
|<span data-ttu-id="878d3-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="878d3-108">HRESULT</span></span>|<span data-ttu-id="878d3-109">Description</span><span class="sxs-lookup"><span data-stu-id="878d3-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="878d3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="878d3-110">S_OK</span></span>|<span data-ttu-id="878d3-111">`GetAssemblyStore` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="878d3-111">`GetAssemblyStore` returned successfully.</span></span>|  
|<span data-ttu-id="878d3-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="878d3-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="878d3-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="878d3-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="878d3-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="878d3-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="878d3-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="878d3-115">The call timed out.</span></span>|  
|<span data-ttu-id="878d3-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="878d3-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="878d3-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="878d3-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="878d3-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="878d3-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="878d3-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="878d3-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="878d3-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="878d3-120">E_FAIL</span></span>|<span data-ttu-id="878d3-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="878d3-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="878d3-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="878d3-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="878d3-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="878d3-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="878d3-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="878d3-124">E_NOINTERFACE</span></span>|<span data-ttu-id="878d3-125">L’hôte ne fournit pas une implémentation de `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="878d3-125">The host does not provide an implementation of `IHostAssemblyStore`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="878d3-126">Notes</span><span class="sxs-lookup"><span data-stu-id="878d3-126">Remarks</span></span>  
 <span data-ttu-id="878d3-127">`IHostAssemblyStore` Fournit des méthodes qui permettent à un hôte à lier aux assemblys et aux modules indépendamment du CLR.</span><span class="sxs-lookup"><span data-stu-id="878d3-127">`IHostAssemblyStore` provides methods that allow a host to bind to assemblies and modules independently of the CLR.</span></span> <span data-ttu-id="878d3-128">Hôtes fournissent généralement des magasins pour autoriser des assemblys à charger à partir d’autres formats que le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="878d3-128">Hosts typically provide assembly stores to allow assemblies to be loaded from formats other than the file system.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="878d3-129">Si l’hôte n’implémente pas `IHostAssemblyStore`, `GetAssemblyStore` doit retourner une valeur HRESULT d’E_NOINTERFACE et doit définir `ppAssemblyStore` avec la valeur null.</span><span class="sxs-lookup"><span data-stu-id="878d3-129">If the host does not implement `IHostAssemblyStore`, `GetAssemblyStore` should return an HRESULT value of E_NOINTERFACE, and should set `ppAssemblyStore` to null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="878d3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="878d3-130">Requirements</span></span>  
 <span data-ttu-id="878d3-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="878d3-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="878d3-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="878d3-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="878d3-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="878d3-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="878d3-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="878d3-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="878d3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="878d3-135">See also</span></span>

- [<span data-ttu-id="878d3-136">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="878d3-136">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [<span data-ttu-id="878d3-137">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="878d3-137">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
