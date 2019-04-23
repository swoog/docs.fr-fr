---
title: IHostMemoryManager::GetMemoryLoad, méthode
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.GetMemoryLoad
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::GetMemoryLoad
helpviewer_keywords:
- IHostMemoryManager::GetMemoryLoad method [.NET Framework hosting]
- GetMemoryLoad method [.NET Framework hosting]
ms.assetid: e8138f6e-a0a4-48d4-8dae-9466b4dc6180
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c43fd1c63b14fc3254044247213bf09453da870e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175433"
---
# <a name="ihostmemorymanagergetmemoryload-method"></a><span data-ttu-id="1c6f2-102">IHostMemoryManager::GetMemoryLoad, méthode</span><span class="sxs-lookup"><span data-stu-id="1c6f2-102">IHostMemoryManager::GetMemoryLoad Method</span></span>
<span data-ttu-id="1c6f2-103">Obtient la quantité de mémoire physique qui est actuellement en cours d’utilisation et par conséquent pas disponible, comme indiqué par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-103">Gets the amount of physical memory that is currently in use, and therefore unavailable, as reported by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c6f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c6f2-104">Syntax</span></span>  
  
```  
HRESULT GetMemoryLoad (  
    [out] DWORD*  pMemoryLoad,   
    [out] SIZE_T  *pAvailableBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1c6f2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c6f2-105">Parameters</span></span>  
 `pMemoryLoad`  
 <span data-ttu-id="1c6f2-106">[out] Pointeur vers le pourcentage approximatif de mémoire physique totale qui est actuellement en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-106">[out] A pointer to the approximate percentage of total physical memory that is currently in use.</span></span>  
  
 `pAvailableBytes`  
 <span data-ttu-id="1c6f2-107">[out] Pointeur vers le nombre d’octets disponibles pour le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-107">[out] A pointer to the number of bytes available to the common language runtime (CLR).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1c6f2-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1c6f2-108">Return Value</span></span>  
  
|<span data-ttu-id="1c6f2-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1c6f2-109">HRESULT</span></span>|<span data-ttu-id="1c6f2-110">Description</span><span class="sxs-lookup"><span data-stu-id="1c6f2-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1c6f2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c6f2-111">S_OK</span></span>|<span data-ttu-id="1c6f2-112">`GetMemoryLoad` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-112">`GetMemoryLoad` returned successfully.</span></span>|  
|<span data-ttu-id="1c6f2-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1c6f2-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1c6f2-114">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1c6f2-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1c6f2-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1c6f2-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-116">The call timed out.</span></span>|  
|<span data-ttu-id="1c6f2-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1c6f2-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1c6f2-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1c6f2-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1c6f2-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1c6f2-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1c6f2-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1c6f2-121">E_FAIL</span></span>|<span data-ttu-id="1c6f2-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1c6f2-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1c6f2-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1c6f2-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1c6f2-125">Remarks</span></span>  
 <span data-ttu-id="1c6f2-126">`GetMemoryLoad` encapsule le Win32 `GlobalMemoryStatus` (fonction).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-126">`GetMemoryLoad` wraps the Win32 `GlobalMemoryStatus` function.</span></span> <span data-ttu-id="1c6f2-127">La valeur de `pMemoryLoad` est l’équivalent de la `dwMemoryLoad` champ dans le `MEMORYSTATUS` structure retournée à partir de `GlobalMemoryStatus`.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-127">The value of `pMemoryLoad` is the equivalent of the `dwMemoryLoad` field in the `MEMORYSTATUS` structure returned from `GlobalMemoryStatus`.</span></span>  
  
 <span data-ttu-id="1c6f2-128">Le runtime utilise la valeur de retour comme une méthode heuristique pour le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-128">The runtime uses the return value as a heuristic for the garbage collector.</span></span> <span data-ttu-id="1c6f2-129">Par exemple, si l’hôte signale que la majorité de la mémoire est en cours d’utilisation, le garbage collector peut choisir de collecter à partir de plusieurs générations afin d’augmenter la quantité de mémoire qui peut potentiellement deviennent disponible.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-129">For example, if the host reports that the majority of memory is in use, the garbage collector may elect to collect from multiple generations to increase the amount of memory that can potentially become available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c6f2-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c6f2-130">Requirements</span></span>  
 <span data-ttu-id="1c6f2-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c6f2-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1c6f2-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1c6f2-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1c6f2-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1c6f2-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c6f2-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c6f2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c6f2-135">See also</span></span>

- <xref:System.GC?displayProperty=nameWithType>
- [<span data-ttu-id="1c6f2-136">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="1c6f2-136">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
