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
ms.openlocfilehash: b5d58a90901b7d7cb80ea7f25401b857b4d4875e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434510"
---
# <a name="iclrerrorreportingmanagerbegincustomdump-method"></a><span data-ttu-id="83a4d-102">ICLRErrorReportingManager::BeginCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="83a4d-102">ICLRErrorReportingManager::BeginCustomDump Method</span></span>
<span data-ttu-id="83a4d-103">Spécifie la configuration des dumps de tas personnalisés pour le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="83a4d-103">Specifies the configuration of custom heap dumps for error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83a4d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83a4d-104">Syntax</span></span>  
  
```  
HRESULT BeginCustomDump (  
    [in] ECustomDumpFlavor dwFlavor,  
    [in] DWORD dwNumItems,  
    [in, size_is(dwNumItems), length_is(dwNumItems)] CustomDumpItem items[],  
    DWORD dwReserved  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="83a4d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83a4d-105">Parameters</span></span>  
 `dwFlavor`  
 <span data-ttu-id="83a4d-106">[in] A [ECustomDumpFlavor](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md) valeur qui indique le genre de dump de tas sur lequel générer le dump de tas personnalisé.</span><span class="sxs-lookup"><span data-stu-id="83a4d-106">[in] A [ECustomDumpFlavor](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md) value that indicates the kind of heap dump upon which to build the custom heap dump.</span></span>  
  
 `dwNumItems`  
 <span data-ttu-id="83a4d-107">[in] La longueur de la `items` tableau.</span><span class="sxs-lookup"><span data-stu-id="83a4d-107">[in] The length of the `items` array.</span></span> <span data-ttu-id="83a4d-108">Si `dwFlavor` n’est pas DUMP_FLAVOR_Mini, `dwNumItems` doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="83a4d-108">If `dwFlavor` is not DUMP_FLAVOR_Mini, `dwNumItems` should be zero.</span></span>  
  
 `items`  
 <span data-ttu-id="83a4d-109">[in] Un tableau de [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) instances, en spécifiant les éléments à ajouter au minidump.</span><span class="sxs-lookup"><span data-stu-id="83a4d-109">[in] An array of [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) instances, specifying the items to add to the mini-dump.</span></span> <span data-ttu-id="83a4d-110">Si `dwFlavor` n’est pas DUMP_FLAVOR_Mini, `items` doit être null.</span><span class="sxs-lookup"><span data-stu-id="83a4d-110">If `dwFlavor` is not DUMP_FLAVOR_Mini, `items` should be null.</span></span>  
  
 `dwReserved`  
 <span data-ttu-id="83a4d-111">[in] Réservé à un usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="83a4d-111">[in] Reserved for future use.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="83a4d-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="83a4d-112">Return Value</span></span>  
  
|<span data-ttu-id="83a4d-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="83a4d-113">HRESULT</span></span>|<span data-ttu-id="83a4d-114">Description</span><span class="sxs-lookup"><span data-stu-id="83a4d-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="83a4d-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="83a4d-115">S_OK</span></span>|<span data-ttu-id="83a4d-116">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="83a4d-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="83a4d-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="83a4d-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="83a4d-118">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="83a4d-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="83a4d-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="83a4d-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="83a4d-120">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="83a4d-120">The call timed out.</span></span>|  
|<span data-ttu-id="83a4d-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="83a4d-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="83a4d-122">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="83a4d-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="83a4d-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="83a4d-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="83a4d-124">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="83a4d-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="83a4d-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="83a4d-125">E_FAIL</span></span>|<span data-ttu-id="83a4d-126">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="83a4d-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="83a4d-127">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="83a4d-127">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="83a4d-128">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="83a4d-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83a4d-129">Notes</span><span class="sxs-lookup"><span data-stu-id="83a4d-129">Remarks</span></span>  
 <span data-ttu-id="83a4d-130">Le `BeginCustomDump` méthode définit la configuration du dump de tas personnalisé.</span><span class="sxs-lookup"><span data-stu-id="83a4d-130">The `BeginCustomDump` method sets custom heap dump configuration.</span></span> <span data-ttu-id="83a4d-131">Le [EndCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md) méthode efface la configuration du dump du tas personnalisé et libère tout état associé.</span><span class="sxs-lookup"><span data-stu-id="83a4d-131">The [EndCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md) method clears the custom heap dump configuration and frees any associated state.</span></span> <span data-ttu-id="83a4d-132">Il doit être appelée une fois que le dump de tas personnalisé est terminé.</span><span class="sxs-lookup"><span data-stu-id="83a4d-132">It should be called after the custom heap dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="83a4d-133">Échec d’appel `EndCustomDump` provoque une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="83a4d-133">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83a4d-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83a4d-134">Requirements</span></span>  
 <span data-ttu-id="83a4d-135">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="83a4d-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83a4d-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="83a4d-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="83a4d-137">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="83a4d-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="83a4d-138">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83a4d-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83a4d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83a4d-139">See Also</span></span>  
 [<span data-ttu-id="83a4d-140">CustomDumpItem, structure</span><span class="sxs-lookup"><span data-stu-id="83a4d-140">CustomDumpItem Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md)  
 [<span data-ttu-id="83a4d-141">ECustomDumpFlavor, énumération</span><span class="sxs-lookup"><span data-stu-id="83a4d-141">ECustomDumpFlavor Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md)  
 [<span data-ttu-id="83a4d-142">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="83a4d-142">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
