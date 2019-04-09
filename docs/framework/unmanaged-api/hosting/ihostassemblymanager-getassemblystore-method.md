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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59092771"
---
# <a name="ihostassemblymanagergetassemblystore-method"></a><span data-ttu-id="ace35-102">IHostAssemblyManager::GetAssemblyStore, méthode</span><span class="sxs-lookup"><span data-stu-id="ace35-102">IHostAssemblyManager::GetAssemblyStore Method</span></span>
<span data-ttu-id="ace35-103">Obtient un pointeur d’interface vers un [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) qui représente la liste des assemblys chargés par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="ace35-103">Gets an interface pointer to an [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ace35-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ace35-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyStore (  
    [out] IHostAssemblyStore **ppAssemblyStore  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ace35-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ace35-105">Parameters</span></span>  
 `ppAssemblyStore`  
 <span data-ttu-id="ace35-106">[out] Un pointeur de fonction vers une `IHostAssemblyStore` de l’instance, ou null si l’hôte n’implémente pas `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="ace35-106">[out] A function pointer to an `IHostAssemblyStore` instance, or null, if the host does not implement `IHostAssemblyStore`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ace35-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ace35-107">Return Value</span></span>  
  
|<span data-ttu-id="ace35-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ace35-108">HRESULT</span></span>|<span data-ttu-id="ace35-109">Description</span><span class="sxs-lookup"><span data-stu-id="ace35-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ace35-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ace35-110">S_OK</span></span>|`GetAssemblyStore` <span data-ttu-id="ace35-111">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="ace35-111">returned successfully.</span></span>|  
|<span data-ttu-id="ace35-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ace35-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ace35-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="ace35-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ace35-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ace35-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ace35-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="ace35-115">The call timed out.</span></span>|  
|<span data-ttu-id="ace35-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ace35-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ace35-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="ace35-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ace35-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ace35-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ace35-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="ace35-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ace35-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ace35-120">E_FAIL</span></span>|<span data-ttu-id="ace35-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ace35-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ace35-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="ace35-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ace35-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="ace35-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ace35-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="ace35-124">E_NOINTERFACE</span></span>|<span data-ttu-id="ace35-125">L’hôte ne fournit pas une implémentation de `IHostAssemblyStore`.</span><span class="sxs-lookup"><span data-stu-id="ace35-125">The host does not provide an implementation of `IHostAssemblyStore`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ace35-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ace35-126">Remarks</span></span>  
 `IHostAssemblyStore` <span data-ttu-id="ace35-127">Fournit des méthodes qui permettent à un hôte à lier aux assemblys et aux modules indépendamment du CLR.</span><span class="sxs-lookup"><span data-stu-id="ace35-127">provides methods that allow a host to bind to assemblies and modules independently of the CLR.</span></span> <span data-ttu-id="ace35-128">Hôtes fournissent généralement des magasins pour autoriser des assemblys à charger à partir d’autres formats que le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ace35-128">Hosts typically provide assembly stores to allow assemblies to be loaded from formats other than the file system.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ace35-129">Si l’hôte n’implémente pas `IHostAssemblyStore`, `GetAssemblyStore` doit retourner une valeur HRESULT d’E_NOINTERFACE et doit définir `ppAssemblyStore` avec la valeur null.</span><span class="sxs-lookup"><span data-stu-id="ace35-129">If the host does not implement `IHostAssemblyStore`, `GetAssemblyStore` should return an HRESULT value of E_NOINTERFACE, and should set `ppAssemblyStore` to null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ace35-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ace35-130">Requirements</span></span>  
 <span data-ttu-id="ace35-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ace35-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ace35-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ace35-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ace35-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ace35-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="ace35-134">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ace35-134">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ace35-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ace35-135">See also</span></span>

- [<span data-ttu-id="ace35-136">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="ace35-136">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [<span data-ttu-id="ace35-137">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="ace35-137">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
