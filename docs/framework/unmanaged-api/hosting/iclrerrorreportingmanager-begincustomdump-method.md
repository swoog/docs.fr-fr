---
title: ICLRErrorReportingManager::BeginCustomDump, méthode
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.BeginCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::BeginCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::BeginCustomDump method [.NET Framework hosting]
- BeginCustomDump method
ms.assetid: 93424a87-ba13-4fa1-b4dc-69d44437b7ae
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8cb6cd8d31e01ea2f1749a6cb4d17173679f0c06
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59104108"
---
# <a name="iclrerrorreportingmanagerbegincustomdump-method"></a><span data-ttu-id="41498-102">ICLRErrorReportingManager::BeginCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="41498-102">ICLRErrorReportingManager::BeginCustomDump Method</span></span>
<span data-ttu-id="41498-103">Spécifie la configuration des dumps de tas personnalisé pour le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="41498-103">Specifies the configuration of custom heap dumps for error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41498-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41498-104">Syntax</span></span>  
  
```  
HRESULT BeginCustomDump (  
    [in] ECustomDumpFlavor dwFlavor,  
    [in] DWORD dwNumItems,  
    [in, size_is(dwNumItems), length_is(dwNumItems)] CustomDumpItem items[],  
    DWORD dwReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="41498-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41498-105">Parameters</span></span>  
 `dwFlavor`  
 <span data-ttu-id="41498-106">[in] Un [ECustomDumpFlavor](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md) valeur qui indique le genre de dump de tas sur lequel générer le dump de tas personnalisé.</span><span class="sxs-lookup"><span data-stu-id="41498-106">[in] A [ECustomDumpFlavor](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md) value that indicates the kind of heap dump upon which to build the custom heap dump.</span></span>  
  
 `dwNumItems`  
 <span data-ttu-id="41498-107">[in] La longueur de la `items` tableau.</span><span class="sxs-lookup"><span data-stu-id="41498-107">[in] The length of the `items` array.</span></span> <span data-ttu-id="41498-108">Si `dwFlavor` n’est pas DUMP_FLAVOR_Mini, `dwNumItems` doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="41498-108">If `dwFlavor` is not DUMP_FLAVOR_Mini, `dwNumItems` should be zero.</span></span>  
  
 `items`  
 <span data-ttu-id="41498-109">[in] Un tableau de [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) instances, en spécifiant les éléments à ajouter au minidump.</span><span class="sxs-lookup"><span data-stu-id="41498-109">[in] An array of [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) instances, specifying the items to add to the mini-dump.</span></span> <span data-ttu-id="41498-110">Si `dwFlavor` n’est pas DUMP_FLAVOR_Mini, `items` doit être null.</span><span class="sxs-lookup"><span data-stu-id="41498-110">If `dwFlavor` is not DUMP_FLAVOR_Mini, `items` should be null.</span></span>  
  
 `dwReserved`  
 <span data-ttu-id="41498-111">[in] Réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41498-111">[in] Reserved for future use.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="41498-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="41498-112">Return Value</span></span>  
  
|<span data-ttu-id="41498-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="41498-113">HRESULT</span></span>|<span data-ttu-id="41498-114">Description</span><span class="sxs-lookup"><span data-stu-id="41498-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="41498-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="41498-115">S_OK</span></span>|<span data-ttu-id="41498-116">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="41498-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="41498-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="41498-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="41498-118">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="41498-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="41498-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="41498-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="41498-120">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="41498-120">The call timed out.</span></span>|  
|<span data-ttu-id="41498-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="41498-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="41498-122">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="41498-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="41498-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="41498-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="41498-124">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="41498-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="41498-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="41498-125">E_FAIL</span></span>|<span data-ttu-id="41498-126">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="41498-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="41498-127">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="41498-127">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="41498-128">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="41498-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="41498-129">Notes</span><span class="sxs-lookup"><span data-stu-id="41498-129">Remarks</span></span>  
 <span data-ttu-id="41498-130">Le `BeginCustomDump` méthode définit la configuration du dump de tas personnalisé.</span><span class="sxs-lookup"><span data-stu-id="41498-130">The `BeginCustomDump` method sets custom heap dump configuration.</span></span> <span data-ttu-id="41498-131">Le [EndCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md) méthode efface la configuration du dump du tas personnalisé et libère tout état associé.</span><span class="sxs-lookup"><span data-stu-id="41498-131">The [EndCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md) method clears the custom heap dump configuration and frees any associated state.</span></span> <span data-ttu-id="41498-132">Il doit être appelée après que le vidage de tas personnalisé est terminé.</span><span class="sxs-lookup"><span data-stu-id="41498-132">It should be called after the custom heap dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="41498-133">Échec d’appel `EndCustomDump` entraîne une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="41498-133">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41498-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41498-134">Requirements</span></span>  
 <span data-ttu-id="41498-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41498-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41498-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="41498-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="41498-137">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="41498-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="41498-138">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41498-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41498-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41498-139">See also</span></span>

- [<span data-ttu-id="41498-140">CustomDumpItem, structure</span><span class="sxs-lookup"><span data-stu-id="41498-140">CustomDumpItem Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md)
- [<span data-ttu-id="41498-141">ECustomDumpFlavor, énumération</span><span class="sxs-lookup"><span data-stu-id="41498-141">ECustomDumpFlavor Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md)
- [<span data-ttu-id="41498-142">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="41498-142">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
