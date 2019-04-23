---
title: ICLRReferenceAssemblyEnum::Get, méthode
ms.date: 03/30/2017
api_name:
- ICLRReferenceAssemblyEnum.Get
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRReferenceAssemblyEnum::Get
helpviewer_keywords:
- ICLRReferenceAssemblyEnum::Get method [.NET Framework hosting]
- Get method, ICLRReferenceAssemblyEnum interface [.NET Framework hosting]
ms.assetid: f21c1612-9c5d-4abc-a337-577086d29c17
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 31d26ed6249bad8a7e2fbaab01264c1b32e1ff55
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59194472"
---
# <a name="iclrreferenceassemblyenumget-method"></a><span data-ttu-id="248ab-102">ICLRReferenceAssemblyEnum::Get, méthode</span><span class="sxs-lookup"><span data-stu-id="248ab-102">ICLRReferenceAssemblyEnum::Get Method</span></span>
<span data-ttu-id="248ab-103">Obtient l’identité d’assembly à l’index fourni.</span><span class="sxs-lookup"><span data-stu-id="248ab-103">Gets the assembly identity at the supplied index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="248ab-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="248ab-104">Syntax</span></span>  
  
```  
HRESULT Get (  
    [in] DWORD dwIndex,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="248ab-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="248ab-105">Parameters</span></span>  
 `dwIndex`  
 <span data-ttu-id="248ab-106">[in] Index de base zéro de l’identité d’assembly à retourner.</span><span class="sxs-lookup"><span data-stu-id="248ab-106">[in] The zero-based index of the assembly identity to return.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="248ab-107">[out] Une mémoire tampon contenant les données d’identité.</span><span class="sxs-lookup"><span data-stu-id="248ab-107">[out] A buffer containing the assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="248ab-108">[in, out] La taille de la `pwzBuffer` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="248ab-108">[in, out] The size of the `pwzBuffer` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="248ab-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="248ab-109">Return Value</span></span>  
  
|<span data-ttu-id="248ab-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="248ab-110">HRESULT</span></span>|<span data-ttu-id="248ab-111">Description</span><span class="sxs-lookup"><span data-stu-id="248ab-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="248ab-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="248ab-112">S_OK</span></span>|<span data-ttu-id="248ab-113">`Get` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="248ab-113">`Get` returned successfully.</span></span>|  
|<span data-ttu-id="248ab-114">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="248ab-114">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="248ab-115">`pwzBuffer` est trop petit.</span><span class="sxs-lookup"><span data-stu-id="248ab-115">`pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="248ab-116">ERROR_NO_MORE_ITEMS</span><span class="sxs-lookup"><span data-stu-id="248ab-116">ERROR_NO_MORE_ITEMS</span></span>|<span data-ttu-id="248ab-117">L’énumération ne contient aucun élément plus.</span><span class="sxs-lookup"><span data-stu-id="248ab-117">The enumeration contains no more items.</span></span>|  
|<span data-ttu-id="248ab-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="248ab-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="248ab-119">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="248ab-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="248ab-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="248ab-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="248ab-121">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="248ab-121">The call timed out.</span></span>|  
|<span data-ttu-id="248ab-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="248ab-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="248ab-123">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="248ab-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="248ab-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="248ab-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="248ab-125">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="248ab-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="248ab-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="248ab-126">E_FAIL</span></span>|<span data-ttu-id="248ab-127">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="248ab-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="248ab-128">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="248ab-128">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="248ab-129">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="248ab-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="248ab-130">Notes</span><span class="sxs-lookup"><span data-stu-id="248ab-130">Remarks</span></span>  
 <span data-ttu-id="248ab-131">`Get` est généralement appelée deux fois.</span><span class="sxs-lookup"><span data-stu-id="248ab-131">`Get` is typically called twice.</span></span> <span data-ttu-id="248ab-132">Le premier appel fournit une valeur null pour `pwzBuffer`et définit `pcchBufferSize` à la taille appropriée pour `pwzBuffer`.</span><span class="sxs-lookup"><span data-stu-id="248ab-132">The first call supplies a null value for `pwzBuffer`, and sets `pcchBufferSize` to the size appropriate for `pwzBuffer`.</span></span> <span data-ttu-id="248ab-133">Le deuxième appel fournit une taille appropriée `pwzBuffer`et contient les données d’identité assembly canonique à l’achèvement.</span><span class="sxs-lookup"><span data-stu-id="248ab-133">The second call supplies an appropriately sized `pwzBuffer`, and contains the canonical assembly identity data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="248ab-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="248ab-134">Requirements</span></span>  
 <span data-ttu-id="248ab-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="248ab-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="248ab-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="248ab-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="248ab-137">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="248ab-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="248ab-138">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="248ab-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="248ab-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="248ab-139">See also</span></span>

- [<span data-ttu-id="248ab-140">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="248ab-140">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="248ab-141">ICLRReferenceAssemblyEnum, interface</span><span class="sxs-lookup"><span data-stu-id="248ab-141">ICLRReferenceAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md)
