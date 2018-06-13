---
title: ICLRGCManager::GetStats, méthode
ms.date: 03/30/2017
api_name:
- ICLRGCManager.GetStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager::GetStats
helpviewer_keywords:
- GetStats method, ICLRGCManager interface [.NET Framework hosting]
- ICLRGCManager::GetStats method [.NET Framework hosting]
ms.assetid: ce259d1d-cd81-4490-a7a1-0d0ea0804872
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 96673049d37034781dff9f206db86a1d5d953d52
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436398"
---
# <a name="iclrgcmanagergetstats-method"></a><span data-ttu-id="ced23-102">ICLRGCManager::GetStats, méthode</span><span class="sxs-lookup"><span data-stu-id="ced23-102">ICLRGCManager::GetStats Method</span></span>
<span data-ttu-id="ced23-103">Obtient un jeu de statistiques actuelles concernant le système de garbage collection du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="ced23-103">Gets a set of current statistics about the common language runtime's garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ced23-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ced23-104">Syntax</span></span>  
  
```  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ced23-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ced23-105">Parameters</span></span>  
 `pStats`  
 <span data-ttu-id="ced23-106">[dans, out] A [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) instance qui contient les statistiques demandées.</span><span class="sxs-lookup"><span data-stu-id="ced23-106">[in, out] A [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) instance that contains the requested statistics.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ced23-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ced23-107">Return Value</span></span>  
  
|<span data-ttu-id="ced23-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ced23-108">HRESULT</span></span>|<span data-ttu-id="ced23-109">Description</span><span class="sxs-lookup"><span data-stu-id="ced23-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ced23-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ced23-110">S_OK</span></span>|<span data-ttu-id="ced23-111">`GetStats` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="ced23-111">`GetStats` returned successfully.</span></span>|  
|<span data-ttu-id="ced23-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ced23-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ced23-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="ced23-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ced23-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ced23-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ced23-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="ced23-115">The call timed out.</span></span>|  
|<span data-ttu-id="ced23-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ced23-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ced23-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="ced23-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ced23-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ced23-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ced23-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="ced23-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ced23-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ced23-120">E_FAIL</span></span>|<span data-ttu-id="ced23-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ced23-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ced23-122">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="ced23-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ced23-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="ced23-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ced23-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ced23-124">Remarks</span></span>  
 <span data-ttu-id="ced23-125">Le CLR calcule et retourne uniquement les statistiques qui sont spécifiées par le `Flags` champ `pStats`.</span><span class="sxs-lookup"><span data-stu-id="ced23-125">The CLR calculates and returns only those statistics that are specified by the `Flags` field of `pStats`.</span></span>  
  
 <span data-ttu-id="ced23-126">Définir le `Flags` une ou plusieurs valeurs de champ la [COR_GC_STAT_TYPES](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stat-types-enumeration.md) énumération pour spécifier les statistiques de la [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="ced23-126">Set the `Flags` field to one or more values of the [COR_GC_STAT_TYPES](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stat-types-enumeration.md) enumeration to specify which statistics in the [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure are to be set.</span></span>  
  
 <span data-ttu-id="ced23-127">Un exemple de l’utilisation est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ced23-127">An example of the usage is as follows:</span></span>  
  
```  
COR_GC_STATS GCStats;  
GCStats.Flags = COR_GC_COUNTS | COR_GC_MEMORYUSAGE;  
pCLRGCManager->GetStats(&GCStats);  
```  
  
## <a name="requirements"></a><span data-ttu-id="ced23-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ced23-128">Requirements</span></span>  
 <span data-ttu-id="ced23-129">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ced23-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ced23-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ced23-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ced23-131">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ced23-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ced23-132">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ced23-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ced23-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ced23-133">See Also</span></span>  
 [<span data-ttu-id="ced23-134">Gestion automatique de la mémoire</span><span class="sxs-lookup"><span data-stu-id="ced23-134">Automatic Memory Management</span></span>](../../../../docs/standard/automatic-memory-management.md)  
 [<span data-ttu-id="ced23-135">COR_GC_STATS, structure</span><span class="sxs-lookup"><span data-stu-id="ced23-135">COR_GC_STATS Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)  
 [<span data-ttu-id="ced23-136">COR_GC_STAT_TYPES, énumération</span><span class="sxs-lookup"><span data-stu-id="ced23-136">COR_GC_STAT_TYPES Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stat-types-enumeration.md)  
 [<span data-ttu-id="ced23-137">Nettoyage de la mémoire</span><span class="sxs-lookup"><span data-stu-id="ced23-137">Garbage Collection</span></span>](../../../../docs/standard/garbage-collection/index.md)  
 [<span data-ttu-id="ced23-138">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="ced23-138">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="ced23-139">ICLRGCManager, interface</span><span class="sxs-lookup"><span data-stu-id="ced23-139">ICLRGCManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md)  
 [<span data-ttu-id="ced23-140">Interfaces d’hébergement CLR</span><span class="sxs-lookup"><span data-stu-id="ced23-140">CLR Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)  
 [<span data-ttu-id="ced23-141">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="ced23-141">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="ced23-142">Hébergement</span><span class="sxs-lookup"><span data-stu-id="ced23-142">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
