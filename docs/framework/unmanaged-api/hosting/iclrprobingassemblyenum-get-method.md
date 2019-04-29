---
title: ICLRProbingAssemblyEnum::Get, méthode
ms.date: 03/30/2017
api_name:
- ICLRProbingAssemblyEnum.Get
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRProbingAssemblyEnum::Get
helpviewer_keywords:
- Get method, ICLRProbingAssemblyEnum interface [.NET Framework hosting]
- ICLRProbingAssemblyEnum::Get method [.NET Framework hosting]
ms.assetid: fdb67a77-782f-44cf-a8a1-b75999b0f3c8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 268462db51435b87194aafc374d5d8e8ec1df165
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638647"
---
# <a name="iclrprobingassemblyenumget-method"></a><span data-ttu-id="a82b8-102">ICLRProbingAssemblyEnum::Get, méthode</span><span class="sxs-lookup"><span data-stu-id="a82b8-102">ICLRProbingAssemblyEnum::Get Method</span></span>
<span data-ttu-id="a82b8-103">Obtient l’identité d’assembly à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="a82b8-103">Gets the assembly identity at the specified index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a82b8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a82b8-104">Syntax</span></span>  
  
```  
HRESULT Get (  
    [in] DWORD dwIndex,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a82b8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a82b8-105">Parameters</span></span>  
 `dwIndex`  
 <span data-ttu-id="a82b8-106">[in] Index de base zéro de l’identité d’assembly à retourner.</span><span class="sxs-lookup"><span data-stu-id="a82b8-106">[in] The zero-based index of the assembly identity to return.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="a82b8-107">[out] Une mémoire tampon contenant les données d’identité.</span><span class="sxs-lookup"><span data-stu-id="a82b8-107">[out] A buffer containing the assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="a82b8-108">[in, out] La taille de la `pwzBuffer` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a82b8-108">[in, out] The size of the `pwzBuffer` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a82b8-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a82b8-109">Return Value</span></span>  
  
|<span data-ttu-id="a82b8-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a82b8-110">HRESULT</span></span>|<span data-ttu-id="a82b8-111">Description</span><span class="sxs-lookup"><span data-stu-id="a82b8-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a82b8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a82b8-112">S_OK</span></span>|<span data-ttu-id="a82b8-113">`Get` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a82b8-113">`Get` returned successfully.</span></span>|  
|<span data-ttu-id="a82b8-114">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="a82b8-114">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="a82b8-115">`pwzBuffer` est trop petit.</span><span class="sxs-lookup"><span data-stu-id="a82b8-115">`pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="a82b8-116">ERROR_NO_MORE_ITEMS</span><span class="sxs-lookup"><span data-stu-id="a82b8-116">ERROR_NO_MORE_ITEMS</span></span>|<span data-ttu-id="a82b8-117">L’énumération ne contient aucun élément plus.</span><span class="sxs-lookup"><span data-stu-id="a82b8-117">The enumeration contains no more items.</span></span>|  
|<span data-ttu-id="a82b8-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a82b8-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a82b8-119">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="a82b8-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a82b8-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a82b8-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a82b8-121">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="a82b8-121">The call timed out.</span></span>|  
|<span data-ttu-id="a82b8-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a82b8-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a82b8-123">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="a82b8-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a82b8-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a82b8-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a82b8-125">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="a82b8-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a82b8-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a82b8-126">E_FAIL</span></span>|<span data-ttu-id="a82b8-127">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a82b8-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a82b8-128">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="a82b8-128">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a82b8-129">Les appels suivants à toute méthode d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="a82b8-129">Subsequent calls to any hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a82b8-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a82b8-130">Remarks</span></span>  
 <span data-ttu-id="a82b8-131">L’identité à l’index 0 est l’identité spécifique à l’architecture de processeur.</span><span class="sxs-lookup"><span data-stu-id="a82b8-131">The identity at index 0 is the identity specific to the processor architecture.</span></span> <span data-ttu-id="a82b8-132">L’identité à l’index 1 est l’assembly d’architecture neutre pour le langage intermédiaire Microsoft (MSIL).</span><span class="sxs-lookup"><span data-stu-id="a82b8-132">The identity at index 1 is the architecture-neutral assembly for Microsoft intermediate language (MSIL).</span></span> <span data-ttu-id="a82b8-133">L’identité à l’index 2 ne contient aucune information de l’architecture.</span><span class="sxs-lookup"><span data-stu-id="a82b8-133">The identity at index 2 contains no architecture information.</span></span>  
  
 <span data-ttu-id="a82b8-134">`Get` est généralement appelée deux fois.</span><span class="sxs-lookup"><span data-stu-id="a82b8-134">`Get` is typically called twice.</span></span> <span data-ttu-id="a82b8-135">Le premier appel fournit une valeur null pour `pwzBuffer`et définit `pcchBufferSize` à la taille appropriée pour `pwzBuffer`.</span><span class="sxs-lookup"><span data-stu-id="a82b8-135">The first call supplies a null value for `pwzBuffer`, and sets `pcchBufferSize` to the size appropriate for `pwzBuffer`.</span></span> <span data-ttu-id="a82b8-136">Le deuxième appel fournit une taille appropriée `pwzBuffer`et contient les données d’identité assembly canonique à l’achèvement.</span><span class="sxs-lookup"><span data-stu-id="a82b8-136">The second call supplies an appropriately sized `pwzBuffer`, and contains the canonical assembly identity data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a82b8-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a82b8-137">Requirements</span></span>  
 <span data-ttu-id="a82b8-138">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a82b8-138">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a82b8-139">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a82b8-139">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a82b8-140">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a82b8-140">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a82b8-141">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a82b8-141">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a82b8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a82b8-142">See also</span></span>

- [<span data-ttu-id="a82b8-143">ICLRProbingAssemblyEnum, interface</span><span class="sxs-lookup"><span data-stu-id="a82b8-143">ICLRProbingAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrprobingassemblyenum-interface.md)
- [<span data-ttu-id="a82b8-144">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="a82b8-144">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
